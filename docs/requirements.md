# Requirements Draft

These requirements describe the planned initial version. Must means required for the core workflow. Should means desirable if time permits. The application has not yet been implemented or tested.

## Functional Requirements

FR-01: Understanding status. Priority: Must.

Students can give each mistake record one status: Not Understood, Partially Understood, or Mastered. They can change and save it after review. Acceptance: Reopening the record shows the saved status, with only one current status.

FR-02: Screenshot import. Priority: Must.

Students can import a question screenshot and view it in the corresponding record. Acceptance: After saving and reopening the record, the same image is displayed.

FR-03: Record details. Priority: Must.

Each record includes a course and topic, with an optional explanation of the mistake. Acceptance: Saving and reopening a record preserves all entered details.

FR-04: Record filtering. Priority: Must.

Students can filter records by course, topic, and understanding status. Acceptance: Results match all selected filters. If no records match, the application displays an empty-results message.

FR-05: Saved data. Priority: Must.

Records, statuses, and screenshots remain available after the application closes. Acceptance: Closing the application normally and reopening it preserves the saved information and images.

## Proposed Quality Requirements

These quality targets are proposals for review before becoming final commitments.

NFR-01: Filtering speed. Priority: Should.

Filtering 100 records should finish within two seconds on the development computer. Acceptance: Measure filtering time and document the computer hardware, Java version, and dataset used.

NFR-02: Invalid image handling. Priority: Must.

Importing an unsupported or unreadable image must display a clear error message and leave existing records unchanged. Acceptance: Attempt an invalid import, then verify that previously saved records remain unchanged.

NFR-03: Readable status. Priority: Should.

Understanding status must use visible text rather than color alone. Acceptance: All three statuses remain distinguishable in grayscale.

## Scope

The proposed image formats are PNG and JPEG. Students enter course and topic labels manually. OCR, AI-generated answers, and automatic assessment of understanding are outside the initial scope.

The platform, storage design, image-size limit, account requirements, and review-date scheduling remain under evaluation. Cloud synchronization and user accounts are not yet project commitments.
