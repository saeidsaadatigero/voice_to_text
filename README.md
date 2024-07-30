# NLP ChatBot Voice To Text

This code is a Python script designed to create a voice-based chatbot using speech recognition and text-to-speech capabilities. It leverages several libraries, including PyTorch, Transformers, SpeechRecognition, gTTS (Google Text-to-Speech), and playsound. Here's a detailed breakdown of its components and functionality:

### Breakdown of the Code

1. **Library Installation**:
   - The script installs necessary libraries such as `SpeechRecognition`, `gTTS`, `playsound`, and `PyAudio` using pip commands.

2. **Importing Modules**:
   - Imports various libraries for audio processing, speech recognition, text-to-speech conversion, and natural language processing.

3. **Audio Device Listing**:
   - `list_audio_devices()`: This function lists all available audio input devices (microphones) on the system. It prints the name and the number of input channels for each device.

4. **Model Loading**:
   - Loads a pre-trained language model (`facebook/opt-1.3b`) and its tokenizer from the Hugging Face Transformers library. This model is used to generate responses based on user input.

5. **Speech Recognition**:
   - `recognize_speech()`: This function listens for audio input from the microphone, recognizes the speech using Google's speech recognition service, and returns the recognized text. It handles errors if the speech is not understood or if there’s a request error.

6. **Text-to-Speech**:
   - `speak_text(text)`: Converts the given text into speech using gTTS and plays it back. The generated audio file is deleted after playback to save memory.

7. **Chatbot Response Generation**:
   - `get_chatbot_response(user_input)`: This function encodes the user's input, generates a response from the chatbot model, and returns the response along with the updated chat history. It uses the model’s ability to maintain context across multiple turns of conversation.

8. **Main Functionality**:
   - The `main()` function initializes audio processing, lists audio devices, and sets up a loop for continuous interaction:
     - It calls `recognize_speech()` to get user input.
     - If recognized, it generates a response using the chatbot model and speaks it out loud.
     - The loop continues until the user says "Goodbye!".

9. **Execution**:
   - The script runs the `main()` function when executed directly.

### Summary
In summary, this code creates a voice-activated chatbot that listens to user speech, processes it to generate a text response using a pre-trained language model, and then speaks the response back to the user. It's designed for interactive voice conversations and can handle simple commands or queries.

https://colab.research.google.com/drive/1PbChf7nYhXo-VU9tawdKvM2vpPPvyKXt
