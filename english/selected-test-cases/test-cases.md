# Selected Test Cases

This document contains selected test cases created during the ListBoxer QA training project.

The test cases were originally created and executed in Jira. This English version was prepared for portfolio presentation.

---

## TC-01 — TESPG177-550

### Verify the ability to create a universal alphanumeric list

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- Alphabetic and Numeric modes are enabled simultaneously.

**Steps:**
1. Enter an alphanumeric value containing Latin letters and digits within the range 0–9999.
2. Click the **Add to List** button or press **Enter**.

**Expected Result:**
A universal alphanumeric list is created. Values containing uppercase/lowercase Latin letters and digits from 0 to 9999 can be added to the list.

---

## TC-02 — TESPG177-552

### Verify the ability to create an alphabetic list

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- Alphabetic mode is enabled.

**Steps:**
1. Enter a value containing Latin letters in uppercase or lowercase with a length of 1–8 characters.
2. Click the **Add to List** button or press **Enter**.

**Expected Result:**
An alphabetic list is created. Only Latin letters with a length of 1–8 characters can be added. Other characters are not accepted.

---

## TC-03 — TESPG177-553

### Verify the ability to create a numeric list

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- Numeric mode is enabled.

**Steps:**
1. Enter a numeric value within the range 0–9999.
2. Click the **Add to List** button or press **Enter**.

**Expected Result:**
A numeric list is created. Only numeric values are added to the list. Letters and other characters are not accepted.

---

## TC-04 — TESPG177-562

### Verify the ability to save a list to a file

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A list has already been created.

**Steps:**
1. Create or open a list.
2. Execute the save command using the menu or **Ctrl+S**.
3. Select a location on the disk.
4. Confirm the save operation.

**Expected Result:**
The list is successfully saved to a file on the disk.

---

## TC-05 — TESPG177-566

### Verify that a saved list file is created in the selected location

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A list has already been created.

**Steps:**
1. Save the list using the menu or **Ctrl+S**.
2. Select a specific location on the disk.
3. Confirm the save operation.
4. Navigate to the selected directory.

**Expected Result:**
The list file is created in the location selected by the user.

---

## TC-06 — TESPG177-592

### Verify that an opened list contains the correct saved data

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A saved list file with known data exists.

**Steps:**
1. Execute the open-file command using the menu or **Ctrl+O**.
2. Select a previously saved list file.
3. Confirm opening the file.
4. Check the contents of the list.

**Expected Result:**
The opened list contains all previously saved data correctly.

---

## TC-07 — TESPG177-606

### Verify that only one Sort Order option can be selected at a time

**Priority:** Trivial

**Preconditions:**
- ListBoxer 1.98 is running.

**Steps:**
1. Locate the **Sort Order** group.
2. Select **Ascending**.
3. Select **Descending**.
4. Check the state of the **Ascending** option.

**Expected Result:**
Only one option can be selected in the **Sort Order** group at a time. Selecting **Descending** automatically deselects **Ascending**.

---

## TC-08 — TESPG177-608

### Verify that the Descending option sorts the list in descending order

**Priority:** Trivial

**Preconditions:**
- ListBoxer 1.98 is running.
- A list containing several elements exists.

**Steps:**
1. Add several elements to the list.
2. Select **Descending** in the Sort Order group.
3. Check the order of the elements.

**Expected Result:**
The list is sorted in descending order.

---

## TC-09 — TESPG177-621

### Verify that an existing list item remains after adding another item

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A working mode is selected.
- A valid value can be entered in the input field.

**Steps:**
1. Enter the first value.
2. Click **Add to List** or press **Enter**.
3. Enter the second value.
4. Click **Add to List** or press **Enter**.
5. Check the list.

**Expected Result:**
The first item remains in the list after the second item is added. Both values are present.

---

## TC-10 — TESPG177-630

### Verify that Clear List removes all data after adding one item

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- The list is empty.

**Steps:**
1. Enter a value in the input field.
2. Click **Add to List** or press **Enter**.
3. Click **Clear List**.
4. Check the list.

**Expected Result:**
All information is removed from the list after clicking **Clear List**.

---

## TC-11 — TESPG177-652

### Verify that Undo cancels only the last action

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A working mode is selected.
- The list is empty.

**Steps:**
1. Add the first item to the list.
2. Add the second item to the list.
3. Open the **Edit** menu.
4. Select **Undo**.
5. Check the list.

**Expected Result:**
Only the last action is cancelled. The second item is removed while the first item remains in the list.

---

## TC-12 — TESPG177-654

### Verify Undo after clearing the list

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.

**Steps:**
1. Add several items to the list.
2. Click **Clear List**.
3. Open the **Edit** menu.
4. Select **Undo**.
5. Check the list.

**Expected Result:**
The last action, clearing the list, is cancelled. The list is restored to its previous state with all items.

---

## TC-13 — TESPG177-657

### Verify that the user can continue working with the list after Undo

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.

**Steps:**
1. Add a new item to the list.
2. Execute **Undo** through the Edit menu.
3. Enter a new value.
4. Click **Add to List** or press **Enter**.
5. Check the list.

**Expected Result:**
The user can continue working with the list without errors after Undo. New items are added correctly.

---

## TC-14 — TESPG177-664

### Verify contextual help via F1 for control elements

**Priority:** Trivial

**Preconditions:**
- ListBoxer 1.98 is running.

**Steps:**
1. Select the following controls one by one:
   - Add to List
   - Clear List
   - Ascending
   - Descending
   - Alphabetic
   - Numeric
2. Press **F1** for each control.
3. Check the application's response.

**Expected Result:**
Contextual help is displayed for each control after pressing **F1**.

---

## TC-15 — TESPG177-677

### Verify Ctrl+Z after adding an item to the list

**Priority:** Major

**Preconditions:**
- ListBoxer 1.98 is running.
- A working mode is selected.

**Steps:**
1. Enter a value in the input field.
2. Click **Add to List** or press **Enter**.
3. Press **Ctrl+Z**.
4. Check the list.

**Expected Result:**
Ctrl+Z cancels the item addition. The added item is removed from the list.