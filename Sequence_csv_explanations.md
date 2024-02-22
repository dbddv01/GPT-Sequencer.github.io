## Understanding the Sequence Structure

The sequence is defined in a tabular format with columns representing different aspects of each step in the sequence:

Hereunder as an example, the breakdown analysis of a sequence named "docu_search5.csv".

Based on a user question, and an uploaded document in the library, the docu_search function will find relevant text chunks (based on semantic similarities result) to the question, the LLM is then instructed to use these text snippets to write down a potential answer to the initial question raised (llm_completion function), the results are then sent as an answer to end-user (user_input).


| Input                                                                                                                                      | Action          | Option                               | next_df                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------|--------------------------------------|------------------------------|
| `{full_prompt}`                                                                                                                            | docu_search     | `{}`                                 | next                         |
| In order to answer the following formulated question : `{full_prompt}`, the hereafter text extract have been found : `{result}`. You must provide a detailed answer using these information or answer that no relevant information has been found. In case of relevant information, use them to formulate your answer, mentioning the source  between brackets (e.g. from (name of the source)). Write you best an final answer here below : | llm_completion | `{'max_length': 768, 'temperature': 0.1}` | next                         |
| `{result}`                                                                                                                                 | user_input      | `{}`                                 | promptchain/docu_search5.csv |

- **input**: The data or query to be processed.
- **action**: The operation to be performed on the input.
- **option**: Additional parameters or settings for the action.
- **next_df**: The filename of the next sequence to load, allowing for chaining sequences together.

## Step-by-Step Process

### Document Search (`docu_search`):
- **Input**: `{full_prompt}` is the placeholder for the user's query. {full_prompt} is here the initial input made by the user in the UI. Value is the same as long it is used in the same session and that sliding memory is not active.
- **Action**: `docu_search` triggers a document search based on the input query. At the moment this a basic function using duckduckgo search.
- **Option**: `{}` indicates no additional options are set for this action.
- **Output**: The action outputs `{result}`, which contains text extracts found relevant to the query.

### Generate Detailed Answer (`llm_completion`):
- **Input**: The text `{result}` from the previous step.
- **Action**: `llm_completion` uses the AI model to generate a detailed answer based on the provided input.
- **Option**: `{'max_length': 768, 'temperature': 0.1}` specifies the maximum length of the generated response and the creativity/variability of the response.
- **Output**: A comprehensive answer utilizing the information found during the document search.

### User Input (`user_input`):
- **Input**: The final answer generated in the previous step.
- **Action**: `user_input` allows the end-user to review the generated answer and make any necessary adjustments or confirmations.
- **Option**: `{}` indicates no additional options are set for this action.
- **Next Step**: Loads the next sequence from `promptchain/docu_search5.csv` for further actions or ends the sequence if no further action is specified.

## Developing Your Own Sequence

End-users can develop their own sequences by following the structure outlined above. They can make such csv with any simple tool (notepad etc), taking in account that separator is a '|' and not a comma. Here are some steps to guide you through creating a custom sequence:

1. **Define the Task**: Start by clearly defining the task you want to automate. Break down the task into steps that can be executed sequentially.
2. **Identify Actions**: For each step, identify the appropriate action (e.g., document search, data analysis, text generation) that needs to be performed. Refer to the available actions in the application documentation.
3. **Specify Options**: Determine if any actions require additional parameters or settings and specify these in the option column.
4. **Chain Sequences**: If the task involves multiple stages, use the `next_df` column to chain sequences together, specifying the filename of the next sequence to load.
5. **Test and Refine**: After defining your sequence, test it with various inputs to ensure it behaves as expected. Refine the sequence as needed based on the results.

By understanding and utilizing the sequence structure, end-users can automate a wide range of tasks, from simple queries to complex data processing workflows. This not only saves time but also enables users to leverage the AI model's capabilities in a structured and automated manner.
The list of functions currently available will be documented in next section. 
