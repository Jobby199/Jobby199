<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #chat-container {
            width: 300px;
            margin: 20px auto;
            border: 1px solid #ccc;
            padding: 10px;
            height: 300px;
            overflow-y: scroll;
        }
        #message-input {
            width: 250px;
            margin-top: 10px;
        }
    </style>
    <script>
        function sendMessage() {
            var messageInput = document.getElementById('message-input');
            var message = messageInput.value;

            if (message.trim() !== '') {
                var chatContainer = document.getElementById('chat-container');
                var newMessage = document.createElement('div');
                newMessage.textContent = message;
                chatContainer.appendChild(newMessage);

                // You would typically send the message to the server here
                // and receive messages from other users in real-time.
                // For simplicity, this example only updates the UI.

                messageInput.value = '';
            }
        }
    </script>
</head>
<body>
    <div id="chat-container"></div>
    <input type="text" id="message-input" placeholder="Type your message...">
    <button onclick="sendMessage()">Send</button>
</body>
</html>

