Silver Companion (银发伴侣) AI助手项目说明

Option 1: English Version (Recommended for GitHub)
Silver Companion 👵👴🤖
Silver Companion is a multimodal AI assistant designed specifically for the elderly. It leverages the Google Gemini Live API to create a natural, accessible, and empathetic "digital companion" that can interact via real-time voice and video.
Instead of typing or navigating complex menus, users simply speak or use hand gestures to interact with the assistant.
✨ Key Features
•Real-time Voice Conversation: Uses low-latency audio streaming for a natural chat experience. The AI speaks slowly, clearly, and patiently (configured via system instructions).
•Visual Awareness (Multimodal): The assistant "sees" the user through the webcam.
•Gesture Recognition: Recognizes waves (to say hello) or thumbs up (for confirmation).
•Object Analysis: Users can hold up items, such as medicine bottles, and ask the AI to read labels or explain instructions.
•Accessibility First UI:
        Large, high-contrast buttons.
•Clear visual status indicators (Listening/Processing).
•Simplified interaction flow.
Empathic Persona: The model is prompted to be a warm, supportive friend ("Silver Companion") rather than a robotic assistant.
🛠️ Tech Stack
•Frontend: React 19 (TypeScript)
•Styling: Tailwind CSS
•AI Model: Google Gemini 2.5 (gemini-2.5-flash-native-audio-preview-09-2025)
•SDK: @google/genai
•Audio: Native Web Audio API (Raw PCM processing for low-latency streaming)
•Video: Real-time Canvas processing and base64 frame injection.
🚀 How It Works
•Connection: Establishes a persistent WebSocket connection with the Gemini Live API.
•Audio Streaming:
        Input: Microphone audio is downsampled to 16kHz PCM and streamed to the model.
•Output: Model audio responses (24kHz) are decoded and played back via the browser's AudioContext.
Video Streaming: Video frames are captured from the webcam, compressed as JPEGs, and sent alongside audio data, allowing the model to correlate speech with visual context in real-time.
📦 Setup
1.Clone the repository.
2.Create a .env file (or set environment variables) with your Google API Key:
bash
API_KEY=your_gemini_api_key_here
3. Open index.html in a modern browser (or serve via a simple HTTP server like vite or http-server).

Option 2: Chinese Version (中文版)
Silver Companion (银发伴侣) 👵👴🤖
Silver Companion 是一个专为老年人设计的多模态 AI 助手。它利用 Google Gemini Live API 构建，提供了一个自然、无障碍且充满人文关怀的“数字伴侣”，支持通过实时语音和视频进行交互。
用户无需打字或浏览复杂的菜单，只需开口说话或使用简单的手势即可与助手互动。
✨ 主要功能
•实时语音对话：利用低延迟音频流技术实现自然的聊天体验。AI 被设定为语速缓慢、发音清晰且极具耐心（通过 System Instructions 配置）。
•视觉感知（多模态）：助手可以通过摄像头“看到”用户。
•手势识别：识别挥手（打招呼）或竖大拇指（确认/点赞）等动作。
•物体分析：老年人可以举起物品（例如药瓶），让 AI 帮忙阅读标签或解释说明书。
•无障碍优先的 UI 设计：
        超大、高对比度的操作按钮。
•清晰的状态指示（正在聆听/连接中）。
•极简的交互流程。
共情人格：模型被设定为一个温暖、支持性的朋友，而不仅仅是一个机器人助手。
🛠️ 技术栈
•前端框架：React 19 (TypeScript)
•样式库：Tailwind CSS
•AI 模型：Google Gemini 2.5 (gemini-2.5-flash-native-audio-preview-09-2025)
•SDK：@google/genai
•音频处理：原生 Web Audio API (Raw PCM 处理以实现低延迟流传输)
•视频处理：实时 Canvas 帧截取与 Base64 帧注入。
🚀 工作原理
•连接建立：与 Gemini Live API 建立持久的 WebSocket 连接。
•音频流传输：
        输入：麦克风音频被降采样为 16kHz PCM 格式并流式传输给模型。
•输出：接收模型的音频响应（24kHz），解码并通过浏览器的 AudioContext 播放。
视频流传输：定期从摄像头捕获视频帧，压缩为 JPEG 并与音频数据一起发送，使模型能够实时结合视觉语境进行理解。
📦 安装与运行
1.克隆本项目。
2.创建 .env 文件（或设置环境变量）并填入您的 Google API Key：
bash
API_KEY=您的_Gemini_API_Key
3. 使用现代浏览器打开 index.html，或通过简单的 HTTP 服务器（如 vite 或 http-server）运行。
