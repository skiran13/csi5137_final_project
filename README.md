# CSI5137 Final Project

## Automatic structuring of Legal metadata using NLP with applications in RE 
In this project we have worked on Sequential Sentence Classification of Indian Case Documents that are verbose. 
Our goal is to adapt this approach to RE specification which draws parallels with legal documents in terms of verbosity. 
We classify the case documents int 13 different Rhetorical Roles as follows:

-	**Preamble (PREAMBLE)**:This section covers the metadata about the judgment document. A classic judgment would start with the court name, party details, lawyers and judge names, and a summary (headnote). This portion would typically end with keywords like (JUDGMENT or ORDER). Some documents also have HEADNOTES and ACTS sections in the beginning. These are also part of the Preamble. 
-	**Facts (FAC)**: This section corresponds to the facts of the court case. It refers to the events in chronological order that led to the case filing. This section will contain information such as (e.g., First Information Report (FIR) at a police station, filing an appeal to the Magistrate) Depositions and proceedings of the current court, and a summary of lower court proceedings.
-	**Ruling by Lower Court (RLC)**: Cases are usually addressed at lower courts and then appealed at higher courts. This portion will have the judgments given by the lower courts (Trial court, High Court) in line with the current appeal to the supreme court. The lower court’s verdict, analysis, and the ratio behind the judgment by the lower court are annotated with this label.
-	**Issues (ISSUE)**: Certain judgments mention the crucial points on which the decision or verdict needs to be delivered. Issues are the legal questions framed nu the court.
-	**Argument by Petitioner (ARG_PETITIONER)**: Arguments put forward by the petitioner’s lawyers. Precedent cases argued by the petitioner’s lawyer will be present in this category. The court discusses these arguments later and belongs as to be relied/not relied upon.
-	**Argument by Respondent (ARG_RESPONDENT)**: This section should hold the respondent’s lawyer’s arguments. 
-	**Analysis (ANALYSIS)**: These are the court’s views which include the court’s discussion on the evidence, facts presented, prior cases, and statutes. Discussions on the relevance of the current case, and observations from the court. It is the parent tag for three tags: PRE-RELIED, PRE-NOT RELIED, and STATUTE i.e., every statement which belongs to these three tags should also be marked as ANALYSIS.
-	**Statute (STA)**: This section includes the court’s discussion on the established laws that can come from several sources: Acts, Articles, Rules, Quotations, Order, Notices, and Notifications.
-	**Precedent Relied (PRE_RELIED)**: Texts in which the court discusses prior case documents, discussions, and decisions that were relied upon by the court for final decisions. 
-	**Precedent not Relied (PRE_NOT_RELIED)**: These are the texts in which the court discusses prior case documents, decisions, and discussions that were not relied upon by the court for final decisions.
-	**Ratio of the decision (RATIO)**: This includes the primary reason given for the application of any legal principle to the legal issue. This section appears right before the final decision by the court.
-	**Ruling by the Present Court (RPC)**:  Final decision of the court with a conclusion and court order following a natural logical outcome of the rationale.
-	**NONE**: Any sentence that does not belong to any of the above categories will be labeled as NONE.

The implementation of this project is in `rhetorical_roles.ipynb` file. The graphs are present in the `Graphs/` folder
