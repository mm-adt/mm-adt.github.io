# mm-ADT
## An Open Source Collective

The mm-ADT software development group is a collection of loosely acquainted
engineers focused on developing mm-ADT compliant technologies.

---

## Roles
* **User**: A consumer of mm-ADT technology.
  * **Contributor**: A user offering mm-ADT features, patches, and support.  
  * **Customer**: A user with an mm-ADT commercial license.
* **Partner**: A producer of mm-ADT technology.
  * **Creator**: A partner who formed or was invited into an mm-ADT project.

All contributors and partners must sign an ICLA or CCLA.

**ICLA**: Individual Contributor License Agreement.  
**CCLA**: Corporate Contributor License Agreement.

---

## Projects
The mm-ADT virtual machine (mm-ADT VM) is the foundational project that defines
the necessary protocols and tooling for all other mm-ADT projects. 

* Every mm-ADT project has a namespace of the form `xyz.mm-adt.org`.
* Every mm-ADT project has its own GitHub repository.
* Every mm-ADT project has a homepage with documentation.
* Every mm-ADT project has a public and a private mailing list.
  * Public mailing lists are how creators support their users (thus, customers).
  * Private mailing lists are how creators discuss internal politics.

The mm-ADT VM private mailing list is the internal communication forum for all mm-ADT partners.

### Project Creation
Any user can propose a project to the mm-ADT VM public mailing list via a`[DISCUSS]` posting. 
The act of proposing a project makes the user a contributor. After a thorough
discussion of the proposal, the contributor can request that their proposal go to `[VOTE]`.
The project is voted on the mm-ADT VM private mailing list. 
Votes are expressed using -1, 0, or +1 with the voting window lasting 1 week. 
The votes are tallied and the result is either positive (approved), neutral (delayed), or negative (denied). 

If the final `[VOTE]` is positive, then a private repository is created for the project. 
At this point, the contributor is a creator (and thus, an mm-ADT partner). A project 
is maintained in a private repository until its debut release. The first release
requires a `[VOTE]` from all mm-ADT partners (mm-ADT VM private mailing list), where all subsequent 
releases are voted by the project creators (project-specific private mailing list).

### Project Deliverables
The project creators must turn in the following items at every release:

* A summary of their changes.
* A license price.
  * The model (subscription, perpetual, etc.) is constrained by RReduX infrastructure.
  * Creators are responsible for setting a price.
  * The submitted license cost is finalized with a `[VOTE]` amongst the creators.
* A revenue distribution.
  * Only creators of that project receive distributions.
  * The submitted distribution can't change until the next release.
  * Creators are paid according to the distribution within 45 days of receipt of revenue.
  * Creators maintain a "1099 direct deposit" relationship with RReduX,Inc.
  * The release distribution requires a `[VOTE]` across all mm-ADT partners.
