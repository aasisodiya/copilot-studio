# Copilot Studio

## QnA

1. How to set or define a list variable in Copilot Studio?

   - Using `Variable management` select `Set a variable value`.
   - Then inside `Set variable` click `Create new` button
   - Then inside `To value` select `Formula` tab then in `fx` you can define list as following

    | Type                    | Value                                   |
    | ----------------------- | --------------------------------------- |
    | Text List               | `["value1","value2","value3"]`          |
    | Number List             | `[1,2,3]`                               |
    | Table (List of Records) | `Table({Name:"Akash"},{Name:"Aditya"})` |

2. How to save inputs from Adaptive Card into Dataverse Table?

   - Click on `+` Icon in the flow, and select `Add a tool`
   - Here search for `New agent flow` and select the same option
   - This will redirect you to the `Agent flows` > `Designer` page.
   - Here set the trigger as `When an agent calls the flow`.
   - Then in the same block, use `Add an input` button to define all the variables that the agent flow will receive. This can be the data that needs to be saved in the row of dataverse table
   - Again click on `+` Icon in the flow, and select `Add a new row`.
   - Here if the setup is done already you can directly set the value for `Table name` and insert the value for respective columns.
   - If any column is not visible, click on `Advanced parameters` dropdown and search for the column there.
   - Now at last again click on `+` Icon in the flow, and select `Respond to copilot`.
   - And you are done. Now you can use this flow from your Agent flow.

3. How to convert a `choice` type to `string` in Copilot Studio?

   - Use `Text()` function
   - Example: `Text(Topic.VarChoice)`

4. How to delete a column in Dataverse Table (encountering dependency issue)

    - In my case dependency was in one of the Table view
    - Go to your Table, and click on Columns
    - Now find the column you want to delete and try deleting, if it fails then click on 3 dots, and select `Advanced` > `Show dependencies`
    - Here you will see the Views if any that are blocking the delete operations
    - Now go to Views Table and select the View that is blocking and remove the column from the view. 
    - Select the column dropdown and click on `Remove` button.
    - Now retry deleting the column.

5. In Copilot Studio can you connect 2 topics?

    - Yes you can

6. How to add variable to text block of adaptive card?

   - In properties of Adaptive Card, You have a drop down to select either `Formula card` or `JSON card`.
   - For now only `Formula card` will allow variable. So select `Formula card`
   - Now go to the `text` proeprty of the one you want to add variable to
   - Now to add a variable you need to append it as `& Topic.Variable`
   - Example: `text :"Thank You. Stay safe"` becomes `text: "Thank You " & Topic.Variable & ". Stay safe"`

7. Why do i see different welcome messages?

   - Every agent has two types of Topics:
     - Custom Topics
     - System Topics
   - Some of which are default and enabled by default.
   - So you need to manually select and disable the one which you don't need.
