# 📘 Catalog and Search Test Cases

## 🧾 Test Case 1 — Catalog Display (FR-CAT-001)

| **Test Case ID** | TC-CAT-001 |
|------------------|------------|
| **Feature** | Catalog Page – Book List |
| **Related FR Code** | FR-CAT-001 |
| **Test Title** | Verify that the Catalog page displays all available books from the data source |
| **Preconditions** | App is launched, user is on `/catalog` route |
| **Test Steps** | 1. Open the application in the browser<br>2. Navigate to the catalog page (`/catalog`)<br>3. Observe the list of books displayed |
| **Expected Result** | The catalog page should display all books available in the `books` data array (title, author, and description should be visible for each item). |
| **Postconditions** | Book list loads correctly, ready for search or purchase. |
| **Status** | Pass / Fail (to be filled after test) |
| **Evidence (Screenshot)** | `testsevidencecatalog_display.png` |

---

## 🧾 Test Case 2 — Search Functionality (FR-SRCH-002)

| **Test Case ID** | TC-SRCH-002 |
|------------------|-------------|
| **Feature** | Catalog Page – Search Function |
| **Related FR Code** | FR-SRCH-002 |
| **Test Title** | Verify that books can be searched by title, author, or description |
| **Preconditions** | Catalog page is loaded, at least one book is available in the catalog |
| **Test Steps** | 1. Go to `/catalog` page<br>2. Locate the search input field (`Search books...`)<br>3. Type part of a book title or author name (e.g., “Lord of the Rings”)<br>4. Observe the catalog results update dynamically |
| **Expected Result** | Only books whose title, author, or description match the search term (case-insensitive) should be displayed. |
| **Postconditions** | Filtered list remains visible until the search bar is cleared. |
| **Status** | Pass / Fail (to be filled after test) |
| **Evidence (Screenshot)** | `testsevidencesearch_functions.png` |
