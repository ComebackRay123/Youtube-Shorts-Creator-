# Youtube-Shorts-Creator-

import os
from PyQt6.QtCore import Qt
from PyQt6.QtWidgets import QWidget, QVBoxLayout, QHBoxLayout, QLabel, QTextEdit
from PyQt6.QtGui import QPixmap

class AboutTab(QWidget):
    def __init__(self):
        super().__init__()

        main_layout = QVBoxLayout()

        # --- Header Layout ---
        header_layout = QHBoxLayout()
        header_layout.setAlignment(Qt.AlignmentFlag.AlignCenter)
        header_layout.setSpacing(10)

        icon_label = QLabel()
        icon_path = os.path.join(os.path.dirname(__file__), "icon.png")
        pixmap = QPixmap(icon_path)
        icon_label.setPixmap(pixmap.scaledToHeight(40, Qt.TransformationMode.SmoothTransformation))

        title_label = QLabel("<h2>YouTube Shorts Creator</h2>")
        header_layout.addWidget(icon_label)
        header_layout.addWidget(title_label)
        main_layout.addLayout(header_layout)

        # --- Info Box ---
        info_box = QTextEdit()
        info_box.setReadOnly(True)
        info_box.setHtml('''
            <p><b>Version:</b> 1.0.0</p>
            <p><b>Developed by:</b>SoloDev</p>
            <p><b>Description:</b> This application helps creators generate short-form videos optimized for YouTube Shorts, TikTok, and Instagram Reels using AI-enhanced editing.</p>

            <h3>✨ Key Features</h3>
            <ul>
                <li>🎙️ AI-powered script and narration using OpenAI & Deepgram</li>
                <li>✂️ Smart segment detection with GPT-based content analysis</li>
                <li>🧠 One-click extract of the most interesting moment</li>
                <li>📐 Orientation-aware video resizing (Portrait, Square, etc.)</li>
                <li>🎞️ Intro clip support with seamless merge</li>
                <li>🔊 Audio ducking control (Light / Medium / Strong)</li>
                <li>🎧 Deepgram voice model selection with preview playback</li>
                <li>💬 Prompt generator with GPT-powered preview</li>
                <li>📼 Video preview player with slider and playback control</li>
                <li>💡 Smart YouTube title, description, and tag generation</li>
                <li>📤 YouTube batch uploader with thumbnail and schedule</li>
                <li>📁 Bulk downloader with dry-run and emoji progress</li>
                <li>⚙️ Raw video editor tab with threaded exporting</li>
                <li>🧪 Multi-threaded GPT/audio/thumbnail generation</li>
                <li>🧹 Reset button to clear all app state</li>
                <li>📋 Scrollable UI for smaller screen support</li>
                <li>🌗 Dark & light theme toggle with persistent state</li>
                <li>🔌 Plugin-ready exporter architecture (YouTube, TikTok, etc.)</li>
            </ul>

            <h3>📁 File Structure</h3>
            <ul>
                <li><code>output_videos/</code> — Final exported clips</li>
                <li><code>output_audio/</code> — Generated AI audio</li>
                <li><code>output_preview/</code> — Preview audio snippets</li>
                <li><code>config/</code> — Auto-saved app settings</li>
                <li><code>output_temp/</code> — Temporary MoviePy files</li>
            </ul>

            <h3>💡 Tips</h3>
            <ul>
                <li>Use “AI-Enhanced Splitting” for more accurate segments</li>
                <li>Include an intro clip to boost branding</li>
                <li>Pick the correct resize mode based on platform (e.g., Shorts = Portrait)</li>
                <li>Use GPT-4o for best results with segmenting and metadata</li>
            </ul>

            <h3>🔧 Requirements</h3>
            <ul>
                <li>Python 3.9+</li>
                <li>PyQt6, MoviePy, OpenAI, Deepgram SDK</li>
                <li>FFmpeg installed and in PATH</li>
            </ul>

            <h3>🔗 Resources</h3>
            <ul>
                <li><a href="https://openai.com/" target="_blank">OpenAI</a> — GPT for scripts and segmentation</li>
                <li><a href="https://deepgram.com/" target="_blank">Deepgram</a> — Voice synthesis</li>
                <li><a href="https://moviepy.org/" target="_blank">MoviePy</a> — Video editing engine</li>
                <li><a href="https://github.com/" target="_blank">GitHub Project (Coming Soon)</a></li>
            </ul>

            <h3>📬 Support</h3>
            <p>If you encounter issues or have suggestions, contact <b>karmakings2024@gmail.com</b></p>
            <p>Happy editing! 🎉</p>
        ''')
        main_layout.addWidget(info_box)
        self.setLayout(main_layout)
