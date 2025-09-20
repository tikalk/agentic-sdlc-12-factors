# VII. Adaptive Quality Gates: Review Appropriately for Each Workflow

*Implement quality assurance practices that are adapted to the specific workflow used to generate the code.*

- [ ] **Perform Micro-Reviews:** During synchronous [SYNC] work, continuously review each small piece of generated code as it's created in real-time.
- [ ] **Enforce Macro-Reviews:** For every PR submitted by an async agent ([ASYNC] work), ensure it passes the full CI pipeline (automated tests, linters, security scans) before you begin a formal human review.
