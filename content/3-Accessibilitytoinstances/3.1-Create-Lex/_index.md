---
title : "Creat Amazon LEX"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---

1. Go to [Amazon LEX console](https://ap-southeast-2.console.aws.amazon.com/lexv2/home).
  + Click on **Create Bot**.

![Configuration](/images/3.connect/Lex-01.png)

2. At the **Step 1: Configure bot settings**.
  + Click to select **Creat a blank bot**.
  + In the **Bot name** section enter **HotelBookingBot**.
  + In the **Description** section enter **Chatbot helps user booking hotel**.

![Configuration](/images/3.connect/Lex-02.png)

   + In the **IAM permissions** section select **Create a role with basic Amazon Lex permissions**.
   + In the **Children's Online Privacy Protection Act (COPPA)** section select **No**.

![Configuration](/images/3.connect/Lex-03.png)

3. At the **Step 2: Add Languages**.
  + Select language as **English(US)**.
  + In the **Voice interaction** section choose **None. This is only a test based application**.
  + Click **Done**.

![Configuration](/images/3.connect/Lex-04.png)


4. Then click on **Intent**.
  + In the **Sample utterances** we will add some sample pharses that we expect a customer would say to invoke the chatbot. We add 3 sentences as the picture bellow.

![Configuration](/images/3.connect/Lex-05.png)


5. Add **Slot type**.
  + Click on **Slot types** in the left menu. We will create our own slot type.
  + Then click on **Add slot type**.
  + In the **Slot type name** enter **RoomType**.
  + In the **Slot value resolution** select **Restrict to slot values**.
  + In the **Slot type values** enter **queen, king and deluxe**.
  + Click on **Save Slot type**.

![Configuration](/images/3.connect/Lex-06.png)

6. Add **Slot**.
  + Now return to **Intent** section.
  + In the **Slot** section we will add some slots that we need the customers to fullfil their information. The chatbot will repeat the question if the information has not been provided.
  + Add 5 prompts for slot, messages and choose the appropriate slot type as the picture bellow.

![Configuration](/images/3.connect/Lex-07.png)

{{% notice note %}}
In the prompt for slot: Room Type choose the Slot type **RoomType** we created before because default AWS does not have this type. 
{{% /notice %}}

7. Add **Confirmation** and **Fulfillment**.
  + In the **Prompts to confirm the intent** section enter **Okay, I have you down for a {Nights} night stay in {Location} starting {CheckInDate}. Shall I book the reservation?**.
  + In the **Responses sent when the user declines the intent** section enter **Okay, I have canceled your reservation**.
  + This prompts will appear to confirm scheduling information. The words in quotes are the Slot above we add. The chatbot will automatically replace these words with the information the customer provide.
  + In the **Fullfilment** section add messages just like the picture bellow.

![Configuration](/images/3.connect/Lex-08.png)

8. In the **Code Hooks - optional** section tick on **Use a Lambda function for intialization and validation**. Now click on **Save intent**.

![Configuration](/images/3.connect/Lex-09.png)

9. First Test

![Configuration](/images/3.connect/Lex-10.png)

We have created and configured Amazon Lex. Now we will move to the next step!

