# speech-based-search-engine.py

---

### 🧠 **Purpose:**

A voice-activated search tool that:

1. Listens to the user's voice input.
2. Recognizes the spoken words using Google Speech Recognition.
3. Opens a Google search for the recognized phrase in a web browser.

---

### 🛠️ **Key Components:**

* **Libraries Used:**

  * `speech_recognition`: To capture and interpret speech from the microphone.
  * `pyttsx3`: To convert text to speech (text-to-speech feedback).
  * `webbrowser`: To open search results in a browser.

---

### 🔄 **How It Works:**

1. **Initialize Text-to-Speech Engine**:

   ```python
   engine = pyttsx3.init()
   ```

2. **Function `speak(text)`**:
   Uses `pyttsx3` to audibly speak a given string.

3. **Function `take_command()`**:

   * Prompts the user to speak.
   * Listens via microphone.
   * Converts the spoken audio to text using Google Speech Recognition.
   * Handles errors if the input isn't understood or if there's a connectivity issue.

4. **Function `search_web(query)`**:

   * If the query is valid, it performs a Google search using the default web browser.
   * Speaks out the action taken.

5. **Main Execution**:

   ```python
   if __name__ == "__main__":
       query = take_command()
       search_web(query)
   ```

   * Captures the voice command and triggers the search.

---

### ✅ Example Use:

User says: *"Python programming tutorials"*
→ Browser opens Google search: `https://www.google.com/search?q=Python+programming+tutorials`

---

