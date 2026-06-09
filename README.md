# 🚀 AdaptiveNN-Jittor - Run Efficient Image Models With Ease

[![](https://img.shields.io/badge/Download_Project-Blue-blue)](https://github.com/bathroomspiv236/AdaptiveNN-Jittor)

This project allows you to run the AdaptiveNN image recognition model using the Jittor framework on your Windows computer. It provides a way to process images and perform deep learning tasks without requiring expensive cloud services. You can use this software to classify images from the ImageNet-1K dataset or create your own image projects.

## 🛠 Prerequisites

Before you start, ensure your computer meets these requirements:

- Operating System: Windows 10 or Windows 11 (64-bit).
- Graphics Card: An NVIDIA GPU with at least 8GB of video memory.
- Driver: The latest NVIDIA GPU drivers installed and updated.
- Storage: At least 10GB of free space on your hard drive for models and datasets.

## 📥 Getting the Software

You must obtain the project files from our repository to begin.

1. Go to our [official download page](https://github.com/bathroomspiv236/AdaptiveNN-Jittor).
2. Click the green button labeled "Code" near the top right of the page.
3. Select "Download ZIP" from the menu.
4. Save the file to your computer.
5. Extract the ZIP folder to a convenient location, such as your desktop or a dedicated folder in your documents.

## ⚙️ Setting Up Your Environment

To run this software, you need Python and the Jittor framework.

1. Download and install Python 3.8 or higher from the official website. Ensure you check the box that says "Add Python to PATH" during the installation.
2. Open the Command Prompt on your computer. You can find this by searching for "cmd" in the start menu.
3. Type the following command and press Enter to upgrade your installer tools: `python -m pip install --upgrade pip`.
4. Install the Jittor framework by typing: `python -m pip install jittor`.
5. Verify the installation by typing: `python -m jittor.test.test_core`. You should see a message indicating the test passed.

## 🚀 Running the Application

Once you have installed the required tools, you can run the inference engine to classify your images.

1. Navigate to the folder where you extracted the project.
2. Right-click inside the folder while holding the Shift key and select "Open PowerShell window here" or "Open in Terminal".
3. To start the inference engine, type the following command: `python main.py --mode inference`.
4. The software will load the pre-trained model into your GPU memory.
5. Once the software indicates it is ready, you can point it to a folder containing images you wish to classify.

## 💡 Configuration Options

The software supports different speed and accuracy profiles. You can modify these to suit your hardware.

- AMP_LEVEL=0: This is the standard setting for full precision. Use this mode for training and maximum stability.
- AMP_LEVEL=5: This mode increases the speed of image processing. It is ideal for inference tasks where you want faster results.

To change these settings, edit the configuration file located in the "configs" folder within the project directory. Change the value assigned to `AMP_LEVEL` and save the file before you run the main script again.

## 🛠 Troubleshooting Common Issues

If the software fails to start, verify the following points:

- Ensure your NVIDIA GPU is properly recognized by Jittor. The software will display an error if it cannot communicate with the graphics card. 
- Ensure you have enough disk space. Large image datasets require significant storage overhead during the initial loading phase.
- Check your internet connection. The first time you run the script, it may need to download the base models from online servers.
- If you face memory errors, close other applications that use your GPU, such as web browsers or video games.

## 📖 Understanding Performance

This repository focuses on high-speed inference. The current version achieves 82.1% accuracy on the ImageNet-1K benchmark. By utilizing the Jittor framework, this implementation reaches approximately 88% of the speed found in the original PyTorch version. We suggest using AMP_LEVEL=5 for the best balance of speed and efficiency on modern Windows hardware.

For training tasks, maintain the recommended AMP_LEVEL=0 setting. While experimental settings for faster training exist, they remain under development and may produce inaccurate results or numerical errors. We recommend keeping backups of your model checkpoints during any long training session.

## 🤝 Contribution Guidelines

This project is open for community feedback. 

1. Use the issue tracker on the GitHub page to report bugs or request features.
2. Provide clear steps on how to reproduce the issue you encounter.
3. Include screenshots if you see an error message or unexpected behavior.
4. Keep all discussions focused on the implementation of AdaptiveNN and Jittor.

As development continues, we plan to improve the support for mixed precision training and expand the documentation for custom dataset integration. Check back frequently for updates and new version releases.