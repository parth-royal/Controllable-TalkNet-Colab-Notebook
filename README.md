## Controllable TalkNet Colab Notebook

This Jupyter Notebook provides a user-friendly interface for using Controllable TalkNet, a model that allows you to synthesize speech and singing voices with fine-grained control over pronunciation and pitch.

### Notebook Walkthrough

The notebook guides you through the following steps:

1. **GPU Check:**
   * Verifies that a GPU has been allocated in Google Colab by running `nvidia-smi -L`.
   * Displays GPU information, including memory usage and compute power.

2. **Dependencies Installation:**
   * Installs necessary packages, including:
     * TensorFlow, Torch, Dash, Jupyter-Dash, psola, wget, unidecode, pysptk, torchvision, torchaudio, torchtext, torch_stft, kaldiio, pydub, pyannote.audio, g2p_en, pesq, pystoi, crepe, resampy, ffmpeg-python, numpy, scipy, NeMo Toolkit, tqdm, gdown, and others.
   * Clones the ControllableTalkNet repository and installs the required packages.
   * Resolves potential package conflicts and compatibility issues with versions.

3. **Running the Interface:**
   * Initializes the ControllableTalkNet interface using the `app.run_server()` function from the `controllable_talknet` module.
   * Optionally sets up a proxy server to access the interface externally if the "inline" mode fails.

### Using the Interface

Once the notebook is running, you can interact with the TalkNet interface:

* **Upload Audio:**  Drag and drop audio clips of a singing or speaking voice into the Files sidebar.
* **Update File List:** Click "Update file list" in the TalkNet interface to refresh the list of available audio files.
* **Select Audio:** Choose an audio file from the dropdown.
* **Transcribe:** Type the text that corresponds to the selected audio clip into the Transcript box.
* **Generate:** Select a character and press "Generate" to synthesize speech or singing. 

### Tips and Tricks

* **Disable Reference Audio:** If you want to use TalkNet as a regular text-to-speech system, tick the "Disable reference audio" checkbox.
* **ARPABET:** You can use ARPABET to override the pronunciation of words (e.g., "{B OW}" for "bow").
* **Short Clips:**  Try working with shorter clips if you run out of memory while generating lines.
* **Singing Model Limitations:**  Singing models are trained on limited data and may have difficulty with certain words. Experiment with ARPABET and punctuation.
* **Pitch Debugging:**  If the voice is off-key, press "Debug pitch" to listen to the extracted pitch.
* **Change Input Pitch:** To adjust the pitch of the generated voice, enable "Change input pitch" and adjust the value in semitones.

### Additional Notes

* **GPU Allocation:** Ensure you have a GPU allocated in Google Colab for optimal performance.
* **Memory Limitations:**  Generating long lines with complex voice effects can be resource-intensive. Use shorter clips or adjust the model settings.
* **Model Specifics:**  The models are trained on specific datasets, so the quality of the generated audio may vary depending on the chosen character and reference audio.

### Contributing

If you have any improvements or suggestions for the notebook or the TalkNet project, please feel free to contribute to the [ControllableTalkNet GitHub repository](https://github.com/emmi-01/ControllableTalkNet).

This README provides a basic overview of the Controllable TalkNet Colab Notebook. For more details, refer to the notebook itself and the [ControllableTalkNet GitHub repository](https://github.com/emmi-01/ControllableTalkNet).


