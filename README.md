<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Robotics Project</title> <!-- Changed title here -->
    <style>
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh; /* Full viewport height */
            background-color: #f0f0f0; /* Light background */
            font-family: Arial, sans-serif; /* Font style */
            text-align: center; /* Center text */
        }
        .message {
            font-size: 24px; /* Font size */
            color: #333; /* Dark text color */
            padding: 20px; /* Padding around the text */
            border: 2px solid #007bff; /* Border color */
            border-radius: 10px; /* Rounded corners */
            background-color: white; /* White background for the message box */
            max-width: 600px; /* Max width for the message box */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Shadow effect */
            white-space: pre-wrap; /* Preserve whitespace */
            overflow: hidden; /* Hide overflow for typing effect */
        }
        .signature {
            margin-top: 20px; /* Space above signature */
            font-weight: bold; /* Bold signature */
            color: #007bff; /* Signature color */
        }
    </style>
</head>
<body>
    <div class="message" id="message"></div>
    <div class="signature">- James Ronda</div>

    <script>
        const messageText = I have crush on you. Di ko alam kung bakit dawa duwang aldaw taka lang na hiling saka dae mo man ako bisto and dae taka man bisto. Diba very non-sense. Merry Christmas btw. The purpose of this is I want to say that i like you.        
        let index = 0;
        const typingSpeed = 50; // Speed of typing in milliseconds

        function typeMessage() {
            if (index < messageText.length) {
                document.getElementById('message').innerText += messageText.charAt(index);
                index++;
                setTimeout(typeMessage, typingSpeed); // Call the function again after typing speed
            }
        }

        typeMessage(); // Start typing the message
    </script>
</body>
