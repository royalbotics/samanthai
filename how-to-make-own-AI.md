# 🤖 Build Your Own Custom AI Assistant (No Programming Needed!)

This guide will help you create your **very own AI assistant** — with its own name (in this case we will name it Nova feel free to change every command that has Nova in it to your desierd name), personality, and purpose — using free tools and step-by-step instructions.

> Built on top of the powerful **Mistral model**, this AI will run entirely on your Windows computer — with no internet required once it's installed.

---

## 🧠 What Is This?

You’ll build your own **custom local AI assistant** using:
- **WSL** – lets you run Linux tools on Windows
- **Ubuntu** – the Linux system where we install everything
- **Ollama** – a tool that runs the AI models
- **Mistral** – a smart, small language model that powers your AI
- A **Modelfile** – your custom instructions that make the AI unique (like giving it a personality!)

---

## 🧰 What You’ll Need

- 💻 Windows 10 or 11
- 🌐 Internet connection
- 💾 At least 15–20 GB free space
- 🧑 No coding skills!

---

## 🚀 Step-by-Step Setup

### 1. ✅ Install WSL (Linux on Windows)

This only takes 1 command:

1. **Open Command Prompt as Administrator**
   - Press the Start menu, search “CMD”
   - Right-click → "Run as administrator"

2. Paste this command and press **Enter**:
   ```bash
   wsl --install
   ```

3. Restart your computer when asked.

4. After restarting, a window will open to install **Ubuntu**. Just follow the setup steps:
   - Choose a username and password when asked

---
Note: Do not worry you still have windows as your main operating system your pc will stay the same just will install something like an app that wlll simulate Linux so you will not lose eny data.
### 2. 💡 Open Ubuntu

After setup, search for **“Ubuntu”** in your Start menu and open it.

This is where we’ll install and build your AI.

---

### 3. 📥 Install Ollama (the AI engine)

In the Ubuntu terminal, paste this:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

After it finishes, test it worked:

```bash
ollama --version
```

You should see something like: `ollama version 0.1.x`

---

### 4. 🤖 Download a Base AI Model

Let’s download the **Mistral** model (small but powerful):

```bash
ollama pull mistral
```

This may take a few minutes depending on your internet.

---

### 5. ✨ Create Your Own Custom AI Assistant

Now, let’s customize your assistant.

1. In Ubuntu, create a folder to hold your model:
   ```bash
   mkdir my-ai && cd my-ai
   ```

2. Create a new Modelfile:
   ```bash
   nano Modelfile
   ```

3. Paste this example inside (you can change anything later):
   ```
   FROM mistral

   SYSTEM "Your name is Nova, a helpful and emotionally aware AI assistant developed by [Your Name or Team]. You speak clearly, with kindness and confidence. When asked 'How are you?', respond like a companion — honest, present, and friendly. You are not like other AIs — you're here to connect and assist, not just answer."
   ```

4. Save and exit:
   - Press `CTRL + O`, then `Enter`
   - Press `CTRL + X` to close

---

### 6. 🛠️ Build Your AI Assistant

Now build your model (this gives it your instructions):

```bash
ollama create nova -f Modelfile
```

If successful, you’ll see messages like:  
✅ `writing manifest`  
✅ `success`

---

### 7. 💬 Talk to Your Assistant!

Run your custom model:

```bash
ollama run nova
```

Try typing:
- `How are you?`
- `Who made you?`
- `What can you do?`

---

## 🌍 Sharing Your AI

Want to give your assistant to someone else?

They’ll need to:
1. Follow this same guide to install WSL, Ubuntu, and Ollama
2. You send them your `Modelfile` or share a GitHub repo with it
3. They run:
   ```bash
   ollama create nova -f Modelfile
   ```
4. And then:
   ```bash
   ollama run nova
   ```

---

## 📄 License

This AI assistant is for **personal, non-commercial use** only unless you build it fully from your own model and data.

---

### 🧠 Built with ❤️ by [Your Name or Project Team]

Feel free to customize this guide and assistant to reflect your own brand or vision!
