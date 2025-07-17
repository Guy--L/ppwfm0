---
marp: true
theme: custom-default
footer: '2025 PPWFM Confidential'
---

# Productivity Pilot
Guy Lister
July 17, 2025
![bg right contain](./img/ascendbars.png)

---

<!-- Speaker Notes -->
# Business Drivers

- Speed to Revenue
- Remove Implementation Bottlenecks per Customer
- Respond to Demand
<!-- Can have multiple on a slide -->

---


# Status Quo

- Many customers in production already
- Databases support current production and are stable
- Years of experience supporting customers has led to exquisite specialization
- Implementation workflow varies from configuration to development
- Setting values in database records by hand


---

# Database Overview (approximate)

<style scoped>
table {
  font-size: 0.75em;
  line-height: 1.1;
  margin: 0 auto;
}
td, th {
  padding: 4px 8px;
}
</style>

| Database           | Tables |
|-------------------|--------|
| Portal             | 98     |
| CalloffPortal      | 89     |
| TwilioIntegration  | 70     |
| RealResponse       | 52     |
| DailyLog           | 27     |
| APIIntegration     | 20     |
| CMSIdentity        | 12     |
| DataSubmit         | 12     |
| MobileIntegration  | 9      |
| CustomImportExport | 8      |
| SFTPIntegration    | 8      |
| WCTPIntegration    | 6      |
| EmailClient        | 5      |
| **Total**          | **416**|

---

# Technical Strategy

- Use API layers to leverage existing database design in new applications
- Use GraphQL to integrate apps across all databases
- Flexibly adapt to new features as customers demand dev
- Listen to and write down use cases from internal experts
- Prioritize and prune dev to match business goals

---

# Tactics

- AI-based development is required
- Bring software best practices to AI
- Unit testing ensures correctness to business
- Combined AI and best practices allow velocity and flexibility
- Tighten the user to dev cycle
- Catch teams up to experts

---

## Appendix

<style scoped>
table {
  font-size: 0.8em;
  line-height: 1.1;
  margin: 0 auto;
}
td, th {
  padding: 4px 8px;
}
</style>

| Feature                               | GraphQL | REST                                  |
| ------------------------------------- | ------- | ------------------------------------- |
| Fetch specific fields                 | ✅       | ❌ (usually returns whole object)      |
| Batch multiple resource requests      | ✅       | ❌ (multiple calls needed)             |
| Strongly typed schema & introspection | ✅       | ❌ (optional OpenAPI)                  |
| Single evolving endpoint              | ✅       | ❌ (many endpoints, versioning issues) |
| Real-time data with subscriptions     | ✅       | ❌ (requires separate setup)           |
| Minimal overfetch/underfetch          | ✅       | ❌                                     |
| Easier client-side flexibility        | ✅       | ❌                                     |
