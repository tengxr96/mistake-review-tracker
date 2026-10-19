# Initial Use Cases

These use cases describe planned behavior. They are not records of completed implementation or testing.

## UC-01: Add a Mistake Record

Actor: Student.

Goal: Save a question screenshot with information that will help organize later review.

Precondition: The application is open and the student has a screenshot available.

Main flow: The student selects Add Record and chooses a screenshot. The application displays a preview. The student enters the course and topic, optionally explains the mistake, and chooses one understanding status. The student selects Save. The application stores the record and associated image and displays the saved record.

Alternate flows: If the image is unsupported or unreadable, the application displays an error and leaves existing records unchanged. The student can choose another image or cancel. If the screenshot, course, topic, or understanding status is missing, the application identifies the missing information and prevents saving. If saving fails, the application reports the failure without claiming success or changing previously saved records. The student can correct the input or storage problem and retry.

Postcondition: A successful save creates a record that can be reopened with its details, status, and screenshot intact. A canceled, invalid, or failed operation creates no successful saved record.

Related requirements: FR-01, FR-02, FR-03, FR-05, FR-06, NFR-02, NFR-03, and NFR-04.

## UC-02: Review and Update Understanding

Actor: Student.

Goal: Review a mistake and record the current level of understanding.

Precondition: At least one mistake record has been saved.

Main flow: The student opens a record and views its screenshot, topic, explanation, and current status. After reviewing the material, the student selects Not Understood, Partially Understood, or Mastered and saves the change. The application stores and displays the selected status. Reopening the record shows that saved status.

Alternate flows: If the student reviews the record without changing its status, the saved status remains unchanged. If saving a changed status fails, the application reports the failure and preserves the previous saved state. The student can retry after correcting the storage problem.

Postcondition: The record retains exactly one saved understanding status.

Related requirements: FR-01, FR-02, FR-03, FR-05, NFR-03, and NFR-04.

## UC-03: Find Topics to Review

Actor: Student.

Goal: Find saved mistakes that match a course, topic, or understanding status.

Precondition: The application is open. The list may contain saved records or be empty.

Main flow: The student opens the record list and selects course, topic, or status filters. The application displays records matching all selected filters. The student opens a matching record to review it using UC-02. Students can use Not Understood and Partially Understood filters to select review priorities based on their own assessments.

Alternate flow: If no records match, including when the list is empty, the application displays an empty-results message. The student can change or clear the filters.

Postcondition: The displayed results match the selected filters; filtering does not change saved records.

Related requirements: FR-04 and NFR-01. Opening and reviewing a result continues through UC-02.

## Requirement Traceability

FR-01 is covered by UC-01 and UC-02 through assigning and updating understanding status.

FR-02 is covered by UC-01 and UC-02 through screenshot import and viewing.

FR-03 is covered by UC-01 and UC-02 through entering and viewing record details.

FR-04 is covered by UC-03 through filtering records and handling empty results.

FR-05 is covered by UC-01 and UC-02 through saving and reopening records.

FR-06 is covered by UC-01 through required-field checks before saving.

NFR-01 applies to filtering in UC-03. NFR-02 applies to invalid imports in UC-01. NFR-03 applies to visible understanding-status labels in UC-01 and UC-02. NFR-04 applies to save failures in UC-01 and UC-02.

## Review Notes

The initial version is a Java Swing desktop application using local storage. No login is required. Screenshots are imported from the student's computer, and topic labels and understanding states are entered manually. Interface layout and storage format will be refined during design. All flows describe planned behavior rather than tested implementation.
