# **English to Hindi Translator**

---

## **Overview**

The English to Hindi Translator is a machine translation system that leverages the MarianMTModel from Hugging Face's Transformers library. It translates English sentences into Hindi using a neural machine translation approach. The system is designed to process English text, translate it into Hindi, and output the translated text.

Currently, the translation system operates with a dataset of English-Hindi sentence pairs. Future enhancements will include better preprocessing techniques and more sophisticated translation features.

---

## **Project Goals**

- **Sentence Translation**: Translate English sentences into Hindi using the MarianMTModel.
- **Training and Fine-Tuning**: Train the model on a custom dataset of English-Hindi sentence pairs.
- **User-Friendly Translation**: Provide a function to easily translate sentences and obtain results in Hindi.

---

## **Features**

- **Custom Dataset**: Utilizes a dataset of English-Hindi sentence pairs for training the model.
- **Translation Model**: Employs MarianMTModel for translating English sentences to Hindi.
- **Training Loop**: Implements a training process with manual tokenization and padding.
- **Translation Function**: Allows translation of individual English sentences into Hindi.

---


## **Dataset**

The dataset used for training consists of English-Hindi sentence pairs stored in `modified_hin.txt`. Examples from the dataset include:

- **Wow!** - **वाह!**
- **Help!** - **बचाओ!**
- **Jump.** - **उछलो.**
- **Hello!** - **नमस्ते।**
- **Cheers!** - **वाह-वाह!**
- **Got it?** - **समझे कि नहीं?**
- **I'm OK.** - **मैं ठीक हूँ।**
- **Awesome!** - **बहुत बढ़िया!**
- **Come in.** - **अंदर आ जाओ।**
- **Get out!** - **बाहर निकल जाओ!**
- **Go away!** - **चले जाओ!**
- **Goodbye!** - **ख़ुदा हाफ़िज़।**
- **Perfect!** - **उत्तम!**
- **Welcome.** - **आपका स्वागत है।**

---

## **Model Architecture**

- **MarianMTModel**: Utilizes Hugging Face's MarianMTModel for machine translation.
- **Feature Extraction**: Extracts features from English sentences for translation to Hindi.
- **Translation Algorithm**: Maps English sentence features to Hindi using the pre-trained MarianMTModel.

---

## **Training**

The model is trained using PyTorch with the following process:

1. **Data Loading**: Loads and preprocesses the dataset with a custom `Dataset` class.
2. **Tokenization & Padding**: Performs manual tokenization and padding of sentences.
3. **Training Loop**: Executes forward and backward passes, computes loss, and updates model parameters.

---

## **Usage**

To translate a sentence from English to Hindi, use the `translate_sentence` function. For example:

```python
english_sentence = "Hello!"
translated_sentence = translate_sentence(english_sentence)
print(f"English: {english_sentence}")
print(f"Hindi: {translated_sentence}")
