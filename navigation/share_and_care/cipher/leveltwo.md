---
layout: base 
title: Levelone 
search_exclude: true
permalink: /leveltwo/
---
# 🔐 **Cipher Challenge: Level 2**

Welcome to **Level** 2 of the Cipher Challenge! 🧩 This level tests your skills with a slightly tougher message. Decode it and advance!



---

## 🔍 **Challenge Objective**

Your goal is to **decode the hidden message** below using a Caesar Cipher technique. Find the hidden word to unlock the path to the next level.

---

## 🧩 **Hints to Get You Started**

1. Each letter in the message has been ****shifted forward by 5**. To decode it, shift each letter **back by 5**.
2. Example: If the coded letter is "F," shifting back by 5 reveals "A."
3. After decryption, the message should be a coherent sentence—trust the flow of the words!

---

## 🔢 **Cipher Text**

Ciphered message:  
`Mtxk, Mtb zlud htj fmnsj? F dtz htwt jzzy jshw ymjwj!`

1. **Hint**: Hint: Shift each letter **back by 5** to reveal the message.
2. **Hint**: Decryption should lead to a phrase that makes logical sense!

---

## 📝 **Submit Your Answer**

Once you’ve cracked the code, submit your answer here:


- **Answer**: `type-your-answer-here`







# Chat Box Demo

This is a basic chat box rendered with HTML inside Markdown.

<div id="chat-container" style="width: 300px; margin: 20px 0; border: 2px solid #ddd; border-radius: 5px; padding: 10px; font-family: Arial, sans-serif;">
  <div id="chat-box" style="height: 200px; overflow-y: scroll; border-bottom: 2px solid #ddd; margin-bottom: 10px; padding: 10px; background-color: #f9f9f9;">
    <div id="chat-messages"></div>
  </div>
  <input type="text" id="chat-input" placeholder="Type a message..." style="width: calc(100% - 60px); padding: 8px; margin-right: 5px; border: 1px solid #ccc; border-radius: 5px;" />
  <button id="send-button" style="padding: 8px; background-color: #007bff; color: white; border: none; border-radius: 5px;">Send</button>
</div>

<script>
  const chatMessages = document.getElementById('chat-messages');
  const chatInput = document.getElementById('chat-input');
  const sendButton = document.getElementById('send-button');
  const correctAnswer = 'Hope, How will you manage? A you move into next level!'; // Define the correct answer here

  function addMessage(text, className) {
    const messageElement = document.createElement('div');
    messageElement.className = className;
    messageElement.textContent = text;
    messageElement.style.margin = '5px 0';
    messageElement.style.padding = '5px';
    messageElement.style.borderRadius = '5px';
    messageElement.style.backgroundColor = className === 'user-message' ? 'black' : 'red';
    chatMessages.appendChild(messageElement);
    chatMessages.scrollTop = chatMessages.scrollHeight;
  }

function addCorrectMessage(text, className) {
    const messageElement = document.createElement('div');
    messageElement.className = className;
    messageElement.textContent = text;
    messageElement.style.margin = '5px 0';
    messageElement.style.padding = '5px';
    messageElement.style.borderRadius = '5px';
    messageElement.style.backgroundColor = className === 'user-message' ? 'black' : 'green';
    chatMessages.appendChild(messageElement);
    chatMessages.scrollTop = chatMessages.scrollHeight;
  }

  sendButton.addEventListener('click', () => {
    const userMessage = chatInput.value.trim();
    if (userMessage) {
      addMessage(`Your answer is: ${userMessage}`, 'user-message');
      chatInput.value = '';

      // Check if the message is correct
      if (userMessage === correctAnswer) {
        setTimeout(() => {
          
          addCorrectMessage("Correct answer! Now you can move on!", 'bot-message');
        }, 1000);
      } else {
        setTimeout(() => {
          addMessage("Try again!", 'bot-message');
        }, 1000);
      }
    }
  });

  chatInput.addEventListener('keypress', (e) => {
    if (e.key === 'Enter') sendButton.click();
  });
</script>


This is a simple interactive chat box. Type a message and hit "Send" or press "Enter" to see it displayed.
