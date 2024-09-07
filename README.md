# RSM-ITD and RSM-CLIP

Welcome to the official repository of our paper **"Rethinking Remote Sensing CLIP: Leveraging Multimodal Large Language Models for High-Quality Vision-Language Dataset"**! This paper has been accepted at **ICONIP 2024**, and we will upload the Arxiv version of the paper soon.

**RSM-ITD** (Remote Sensing Multisource Image-Text Dataset) is a high-quality paired dataset of remote sensing images and captions. **RSM-CLIP** is the fully fine-tuned CLIP model based on RSM-ITD. RSM-CLIP surpasses previous models on various downstream tasks while using much less data compared to other similar models, proving the high quality of RSM-ITD.

We are providing our training data and state-of-the-art models here to promote research progress in the community.

## 1. RSM-ITD Dataset

The file `RSMITD.csv` provides the captions for the dataset.

You can download our dataset images via Baidu Netdisk:

**Link**: [https://pan.baidu.com/s/1n9lsiyzjYOsDc6W4d4imoQ?pwd=vucz](https://pan.baidu.com/s/1n9lsiyzjYOsDc6W4d4imoQ?pwd=vucz)  
**Extraction Code**: `vucz`

demo

![demo](https://github.com/user-attachments/assets/30e8da78-4a18-4de6-8b83-cfa0126b1a6b)




## 2. Usage of the RSM-CLIP Model

### Installation Instructions

Our model is based on **openCLIP**, so please install the necessary dependencies for openCLIP before using the model. You can find the instructions here: [openCLIP GitHub repository](https://github.com/mlfoundations/open_clip).

Additionally, if you want to use our **cross-modal retrieval testing script** (`RET3_RetrieveTest.py`) for benchmarking or reproducing state-of-the-art (SOTA) results, please install the required dependencies mentioned in the script file. Specifically, you need to install `clip_benchmark` via:

```bash
pip install clip_benchmark
```

You will also need to download the following datasets for testing:

- **RSITMD**: [RSITMD GitHub repository](https://github.com/xiaoyuan1996/AMFMN/blob/master/RSITMD/README.md)
- **RSICD**: [RSICD GitHub repository](https://github.com/201528014227051/RSICD_optimal)
- **UCMCaption**: [UCMCaption on AIStudio](https://aistudio.baidu.com/datasetdetail/90740)

### Testing Commands

To test the model, you can use the following command:

```bash
/path/to/python /path/to/your_project/your_script.py \
--model-name "ViT-B-32" \
--retrieval-images-dir "/path/to/images" \
--retrieval-json-dir "/path/to/dataset.json" \
--RSM_CLIP_path "/path/to/RS-CLIP-models/RSM-CLIP-ViT-B-32.pt"
```

## 3. License

This project is licensed under the **Apache 2.0** license. See the [LICENSE](./LICENSE) file for more details.
```
