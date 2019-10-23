---
layout: default
---

# mm-ADT
## A Career-Centric Open Source Model

---

mm-ADT&#8482; is composed of professional developers collaborating on and across any number of self-governed, open source projects. Project members define, develop, support, and market their projects' products. Unlike the free open source models, project members also determine product licensing costs as well as project member revenue distribution percentages. These economic decisions are made in the same manner in which all other project decisions are made&mdash;via `[DISCUSS]` and `[VOTE]`.

<div class="boxed">
<center>
The mm-ADT Open Source Model is currently under development and will not be considered binding until this notice is removed.
</center>
</div>

---

## People

<rimg><a href="assets/images/posters/moments-with-genius.jpg"><img src="assets/images/posters/moments-with-genius.jpg" width="180"/></a></rimg>mm-ADT technologies are produced and consumed by people and companies. Particular roles are identified below and will be refered to throughout the remainder of this document.

**User**: A consumer of mm-ADT technology.  
&nbsp;&nbsp;**Contributor**: A user offering mm-ADT features, patches, and support.  
&nbsp;&nbsp;**Customer**: A user with an mm-ADT commercial license.  
**Partner**: A producer who created or joined an mm-ADT project.
&nbsp;&nbsp;**Member**: A partner in the context of a particular project.  

All contributors and partners must sign an ICLA or CCLA. Each mm-ADT project's GitHub repository must be connected with <a href="https://www.clahub.com/">CLAHub</a>. All contributors are then required to sign the project's ICLA before committing source code.

**ICLA**: Individual Contributor License Agreement (example ICLA for <a href="https://www.clahub.com/agreements/mm-adt/vm">mm-ADT VM</a>).  
**CCLA**: Corporate Contributor License Agreement.

---

## Projects
<rimg><a href="assets/images/posters/work-promotes-confidence.jpg"><img src="assets/images/posters/work-promotes-confidence.jpg" width="180"/></a></rimg> The mm-ADT virtual machine ([mm-ADT VM](http://vm.mm-adt.org/)) is the founding project that is responsible for defining the protocols and tooling by which all other mm-ADT projects integrate.

Every project has an <a href="https://github.com/mm-adt">mm-ADT GitHub repository</a>.  
-- All repositories are hosted in the mm-ADT GitHub organization (example repository for <a href="https://github.com/mm-adt/vm">mm-ADT VM</a>).  

Every project has a namespace structured as `xyz.mm-adt.org`.  
-- Namespaces are managed via DNS CNAMES and <a href="https://redirect.name">redirect.name</a>.  

Every project (of significant complexity) should have <a href="http://twitter.com">Twitter</a> account.  

Every project has a homepage with documentation.  

Every mm-ADT project has a public and a private mailing list.  
-- Public mailing lists are how creators support their users (thus, customers).  
-- Private mailing lists are how creators discuss internal politics.  
--- The mm-ADT VM private mailing list is the internal communication forum for all mm-ADT partners.  

A project's public mailing list is the primary communication medium for interacting with users. All support related questions are handled through a project's public mailing list.

### Project Creation
<rimg><a href="assets/images/posters/free-classes.jpg"><img src="assets/images/posters/free-classes.jpg" width="180"/></a></rimg>Any user can propose a project to the mm-ADT VM public mailing list via a`[DISCUSS]` posting. The act of proposing a project makes the user a contributor. After a thorough discussion of the proposal, the contributor can request that their proposal go to `[VOTE]`. The project is voted on the mm-ADT VM private mailing list. Votes are expressed using -1, 0, or +1 with the voting window lasting 1 week. The votes are tallied and the result is either positive (approved), neutral (delayed), or negative (denied). 

If the final `[VOTE]` is positive, then a private repository is created for the project. At this point, the contributor is an mm-ADT partner. A project is maintained in a private repository until its debut release. The first release requires a `[VOTE]` from all mm-ADT partners (via the mm-ADT VM private mailing list), where all subsequent releases are voted on by the project creators using their project-specific private mailing list.

### Product Release Requirements
<rimg><a href="assets/images/posters/let-me-do-the-talking.jpg"><img src="assets/images/posters/let-me-do-the-talking.jpg" width="180"/></a></rimg>The project members must turn in the following items at every release.

#### A Packaged Product

Maven3-based projects should use <a href="https://creadur.apache.org/rat/">Apache Rat</a> to verify copyright notices (see example <a href="https://github.com/mm-adt/vm/blob/master/java/pom.xml#L118-L157">pom.xml</a>).

#### A Product List Price
-- Partners are responsible for setting their product's price.
-- Pricing should be based on the means of deployment and use (per node, per user, etc.).  
-- The submitted license cost is finalized with a `[VOTE]` amongst the creators.  
-- Pricing models will be contrained by the current RReduX,LLC. infrastructure.  

In order to reduce overhead, prices will be static (non-negotiable) and licenses can be purchased through a web-interface.


#### Revenue Distribution Model

-- Only members of the project receive distributions.  
-- The submitted distribution can't change until the next release.  
-- Project members are paid within 45 days of receipt of revenue.  
-- Creators maintain a "1099 direct deposit" relationship with RReduX,Inc.  
-- The release distribution requires a `[VOTE]` across all mm-ADT partners.  
