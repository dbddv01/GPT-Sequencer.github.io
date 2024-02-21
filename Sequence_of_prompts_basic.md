## Understanding and Modifying Sequence CSV Files

This section of the documentation explains how to understand and modify the sequence CSV files that steer the prompt manipulation submitted to the AI Language Model (LLM). We will use a basic summarization example to illustrate how to modify the default sequence and create a new sequence file.

### Step 1: Starting with the Default Sequence
![Starting with the Default Sequence](/images/110-sequence-start.png)

The default sequence file contains the basic structure for submitting prompts to the LLM. Each row defines a step in the sequence, including inputs, actions, and options.

### Step 2: Modifying the Sequence
![Modifying the Sequence](/images/120-sequence-modify.png)

To modify a sequence, you can change the parameters in the `option` column to adjust the behavior of the LLM. This includes settings such as `max_length` and `temperature`.

### Step 3: Customizing the Prompt
![Customizing the Prompt](/images/130-sequence-modify-prompt.png)

Customize the `input` column to change the prompt sent to the LLM. For instance, to perform summarization, you might start your prompt with "Summarize this: " followed by the text to be summarized.

### Step 4: Saving the New Sequence File
![Saving the New Sequence File](/images/135-sequence-modify-filename.png)

Once you have made your changes, you will need to save the new sequence. Enter the desired filename in the CSV save path.

### Step 5: Verifying the Save
![Verifying the Save](/images/140-sequence-saveas.png)

After saving, ensure that the sequence has been saved correctly by checking the status message and the file path.

### Step 6: Loading the New Sequence File
![Loading the New Sequence File](/images/150-sequence-load.png)

To use your new sequence, load it by selecting the file from the dropdown list and confirming it in the Active Sequence file section.

### Step 7: Working with the Summarizer Sequence
![Working with the Summarizer Sequence](/images/160-sequence-load.png)

Once the new summarizer sequence is active, you can begin using it to submit summarization prompts to the LLM.

### Step 8: Seeing the Summarizer in Action
![Seeing the Summarizer in Action](/images/165-sequence-summarizer.png)

Finally, observe the summarizer sequence working with the chatbot interface, where you can input longer texts and receive summarized responses based on your customized sequence.

