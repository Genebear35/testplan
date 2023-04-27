# testplan
@Test

public void testCreateTodoItem() {

    // Set up test data

    String itemName = "Finish report";

    String itemDescription = "Write final report for GitHub project";

    Date dueDate = new Date(2023, 05, 15);

    int userId = 1;

    

    // Execute the method being tested

    TodoItem newItem = todoService.createTodoItem(itemName, itemDescription, dueDate, userId);

    

    // Assert that the result is as expected

    assertEquals(itemName, newItem.getName());

    assertEquals(itemDescription, newItem.getDescription());

    assertEquals(dueDate, newItem.getDueDate());

    assertEquals(userId, newItem.getUserId());

}

@Test

public void testUpdateTodoItem() {

    // Set up test data

    TodoItem existingItem = new TodoItem(1, "Finish report", "Write final report for GitHub project", new Date(2023, 05, 15), 1);

    String newName = "Submit report";

    String newDescription = "Submit final report for GitHub project";

    Date newDueDate = new Date(2023, 05, 16);

    

    // Execute the method being tested

    TodoItem updatedItem = todoService.updateTodoItem(existingItem.getId(), newName, newDescription, newDueDate);

    

   

