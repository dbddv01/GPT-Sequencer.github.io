## Document Ingestion and Query Handling in GPT Sequencer

### Overview
The GPT Sequencer streamlines document processing and enables users to pose questions directly to uploaded documents. This markdown documentation, along with the provided images from the `/images` directory on GitHub, will guide you through the process of uploading a document, embedding it into the system, and querying it for information.

### Step-by-Step Guide

#### Uploading and Embedding a Document
1. **Starting the Process:**

    - Click on `Upload Text` in the GPT Sequencer interface to upload a new document.
      
     ![Starting the Process](/images/200_ingestpdf_upload.png)
   
   - Choose your desired .pdf (or .txt or .epub)  to upload; in my example i have this file on my local HD, "Arxiv-MemoryBank for LLM-2305.10250.pdf".
     
     ![Choosing PDF](/images/210_ingestpdf_upload.png)
   
3. **Document Processing:**
   - After selecting the document, the system begins processing for ingestion and embedding.
     
     ![Document Processing](/images/220_ingestpdf_embedding_processing.png)
     
   - Once processing is complete, a status message confirms the embedding with a `Text_id` reference.
     
     ![Embedding Confirmation](/images/230_ingestpdf_embedding_processing_done.png)

4. **Updating the Document Library:**
   - To update the library with the newly ingested document, click `Update list`.
     
     ![Updating Library](/images/240_ingestpdf_update_library.png)
     
   - The document now appears in the list of selectable documents.
     
     ![Document List Update](/images/250_ingestpdf_select_document.png)

#### Executing a Document Search Sequence
4. **Loading the Sequence:**
   - To load the document search sequence, click on `Load Sequence.` and select the appropriate Sequence (.csv) file, e.g.: "docu_search5.csv". I advise to uncheck the `Sliding memory` as well.
     
     ![Loading Sequence](/images/270_load_docsearch_sequence.png)
     ![Sequence Selection](/images/272_load_docsearch_sequence.png)

#### Querying the Document:
5. **Asking Your Question:**
   - Input your query into the 'Input' field. Here for example: *"What are the different memorization categories explained in the document?"*
   - Press the enter key to submit the question.
     ![Input Question](/images/275_ask_your_question_press_enter_and_wait.png)

6. **Reading the Answer:**
   - Once the Sequencer processes your question, the answer will be displayed in the 'Chat output' section. It can take a while or not depending on your setup. On my old son gaming pc, it took 180 sec.
   - Read through the provided answer to ensure it meets your expectations and requirements. You may copy the content ;-)
     ![Read Answer](/images/277_read_the_answer.png)

7. **Checking the Log (if needed):**
   - If you need more details on the operations carried out or the data used to generate the answer, refer to the 'Log' tab.
   - The log provides a detailed breakdown of the steps executed, including the search results and any intermediate outputs. Readability could be improved but well, it should give you an idea of the steps taken by the sequence. 
     ![Check Log](/images/280_check_the_log_if_needed.png)

### Conclusion
This guide has walked you through the GPT Sequencer's process for uploading and querying documents. It ensures that you can manage and retrieve information from your documents efficiently and with ease, leveraging the power of AI to interact with your uploaded content.
