# Selected Bug Reports

This document contains selected defects reported during the ListBoxer QA training project.

The defects were originally discovered, documented, and reported in Jira. This English version was prepared for portfolio presentation.

The Jira issue IDs and original priorities are preserved.

---

## BUG-01 — TESPG177-683

### The first saved record is missing after opening a previously saved list

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A previously saved list containing values from 1 to 10 exists.

**Steps to Reproduce:**
1. Execute the Open command using the menu or `Ctrl+O`.
2. Select the previously saved list file.
3. Confirm opening the file.
4. Check the contents of the list.

**Actual Result:**
The first saved record is missing after opening the file. The remaining records are loaded correctly.

**Expected Result:**
The opened list should contain all previously saved data.

---

## BUG-02 — TESPG177-722

### One record is missing after clearing the current list and opening a saved file

**Priority:** Trivial

**Preconditions:**
- ListBoxer 1.98 is running.
- A saved list with a known number of elements exists.

**Steps to Reproduce:**
1. Open a previously saved list.
2. Add a new element to the list.
3. Click **Clear List**.
4. Open another saved list file.
5. Check the number of elements.

**Actual Result:**
One record is missing after opening the saved file.

**Expected Result:**
The opened list should contain all saved elements without data loss.

---

## BUG-03 — TESPG177-713

### Reopening the same saved list adds an empty record and increases the number of elements

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A saved list containing 11 elements exists.

**Steps to Reproduce:**
1. Open the previously saved list.
2. Check the number of elements.
3. Close the list.
4. Open the same file again.
5. Check the number of elements.

**Actual Result:**
An empty record is added after reopening the file. The number of elements increases, for example, from 11 to 12.

**Expected Result:**
The number of elements after opening the file should match the saved data. No additional records should be created.

---

## BUG-04 — TESPG177-724

### Ctrl+Z leaves an empty record after cancelling the addition of an item

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A working mode is selected.

**Steps to Reproduce:**
1. Enter a value in the input field.
2. Click **Add to List** or press **Enter**.
3. Press `Ctrl+Z`.
4. Check the list.

**Actual Result:**
The added item is removed, but an empty record remains in its place. The record counter is not updated.

**Expected Result:**
The item addition should be completely cancelled. The added record should be removed without leaving an empty record.

---

## BUG-05 — TESPG177-684

### Descending option does not sort the list correctly

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.

**Steps to Reproduce:**
1. Add several elements to the list.
2. Select **Descending** in the **Sort Order** group.
3. Check the order of the displayed elements.

**Actual Result:**
The list is not sorted correctly in descending order. Some values are ordered correctly, while other values, including 1 and 2, are displayed in an incorrect order.

**Expected Result:**
The entire list should be sorted in descending order when **Descending** is selected.

---

## BUG-06 — TESPG177-689

### Clear List remains disabled after adding one item

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.

**Steps to Reproduce:**
1. Enter a value in the input field.
2. Click **Add to List** or press **Enter**.
3. Attempt to click **Clear List**.
4. Check the list.

**Actual Result:**
The **Clear List** button remains disabled after adding one item and the list cannot be cleared.

**Expected Result:**
All entered information should be removed after clicking **Clear List**.

---

## BUG-07 — TESPG177-690

### Undo from the Edit menu does not cancel the addition of an item

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A working mode is selected.
- The list is empty.

**Steps to Reproduce:**
1. Enter a value in the input field.
2. Click **Add to List** or press **Enter**.
3. Open the **Edit** menu.
4. Select **Undo**.
5. Check the list.

**Actual Result:**
The last action is not cancelled. The added item remains in the list and the record counter is not decreased.

**Expected Result:**
The last action should be cancelled after selecting **Undo** from the Edit menu.

---

## BUG-08 — TESPG177-691

### Records in list counter is not restored after Undo following Clear List

**Priority:** Minor

**Preconditions:**
- ListBoxer 1.98 is running.

**Steps to Reproduce:**
1. Add several elements to the list.
2. Click **Clear List**.
3. Open the **Edit** menu.
4. Select **Undo**.
5. Check the list and the **Records in list** counter.

**Actual Result:**
The list is restored, but the **Records in list** counter remains `0`.

**Expected Result:**
The Clear List action should be cancelled and the list should return to its previous state.

---

## BUG-09 — TESPG177-709

### F1 opens Microsoft Windows Help instead of ListBoxer contextual help

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- An application control is available.

**Steps to Reproduce:**
1. Press `F1`.
2. Check the result.

**Actual Result:**
An external Microsoft Windows Help and Learning website is opened.

**Expected Result:**
Contextual help for the ListBoxer application should be displayed according to the requirements.

---

## BUG-10 — TESPG177-710

### Ctrl+C does not copy a selected list item and instead changes focus to an item beginning with C

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- The list contains at least one element.

**Steps to Reproduce:**
1. Select an element in the list.
2. Press `Ctrl+C`.
3. Attempt to paste the value into the input field or another application.

**Actual Result:**
The selected value is not copied to the clipboard. When the list has focus, the application instead moves the focus to an item beginning with `C` or `c`.

**Expected Result:**
The selected list item should be copied to the clipboard after pressing `Ctrl+C`.