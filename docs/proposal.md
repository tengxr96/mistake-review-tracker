# Project Proposal

## Problem and Need

I currently do not save the questions I answer incorrectly. During exam preparation, I find it difficult to identify my weak topics. Mistake Review Tracker will help students keep question screenshots together with course labels, topic labels, error explanations, and self-reported understanding.

The need is supported by my own learning experience. Interviews, surveys, and evidence of improved academic performance have not been collected. The project aims to support review decisions; its benefits will need evaluation with actual use.

## Stakeholders

The primary users are students who want to organize mistakes and decide what to review. They need readable screenshots, useful course and topic filters, and a simple way to update their understanding after review.

I am the sole developer and initial user. I am responsible for requirements, design, implementation, verification, and documentation. My concerns are manageable scope, reliable saved records, and the time needed to learn interface development. If the application is maintained later, clear documentation and understandable Java code will help its maintainer.

## Objectives and Scope

The initial version will import and display question screenshots, save course and topic information with an optional error explanation, and assign one of three statuses: Not Understood, Partially Understood, or Mastered. Students will update these statuses after review and filter records by course, topic, or status. Saved information and screenshots will remain available after the application closes.

The supported image formats will be PNG and JPEG. Classification and understanding status are entered by the student. The initial version will be a local Java Swing desktop application. OCR, automatic answer generation, automatic diagnosis of understanding, Canvas integration, accounts, cloud synchronization, and scheduled review reminders are outside its scope.

## Feasibility

Java is the language I am most familiar with. The planned Swing desktop interface and local storage support file selection, image display, forms, and record lists. I have not previously developed a Java graphical interface, so this part requires learning and an early prototype. The exact storage format remains to be selected.

The initial technical milestone will demonstrate importing an image, displaying it with a record, saving the record, and reopening it. This will test the main technical assumptions before the complete interface is built. The work has not yet been performed.

The plan uses one developer and a limited workflow. No paid hosting or external AI service is planned. The implementation schedule must account for interface and persistence learning. If time becomes limited, essential screenshot, status, filtering, and persistence functions take priority over optional enhancements.

Students must manually label records and update their understanding. To evaluate whether this effort is practical, I plan to try the workflow with examples from one course and record any usability problems. Additional student feedback will be sought if available; it has not yet been obtained.

## Risks and Success Criteria

The main risks are GUI learning time, broken image references, data loss, inconsistent topic labels, and users forgetting to update their status. Early import and persistence prototypes, controlled topic labels where practical, and clear status text are proposed ways to reduce these risks.

A successful initial version will let a student save a screenshot with its details, retrieve it after restarting, change its understanding status, and find records using the required filters. Correctness will be evaluated against the acceptance criteria in docs/requirements.md. These criteria describe planned checks, not completed test results.
