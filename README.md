# MedDef Paper - Neurocomputing Submission

This repository contains the LaTeX source for "MedDef: An Efficient Self-Attention Model for Adversarial Resilience in Medical Imaging with Unstructured Pruning" - a research paper submitted to Neurocomputing journal.

## 🔗 **Public Repository Access**

> **📂 Complete Project Download:**  
> **🌐 [https://github.com/Hetawk/elsevier_neurocomputing.git](https://github.com/Hetawk/elsevier_neurocomputing.git)**
>
> **Quick Clone:**
>
> ```bash
> git clone https://github.com/Hetawk/elsevier_neurocomputing.git
> cd elsevier_neurocomputing
> make main  # Build the paper
> ```

## 📁 Project Structure

```
├── main.tex                    # Main manuscript
├── main.pdf                   # Compiled PDF output
├── abstract.tex               # Abstract document (separate for submission)
├── abstract.pdf              # Compiled abstract PDF
├── declaration_interests.tex  # Declaration of interests (separate for submission)
├── declaration_interests.pdf # Compiled declaration PDF
├── Makefile                   # Build automation
├── README.md                  # This file
├── elsarticle-num.bst        # Elsevier bibliography style
├── fig/                      # Figures and images
│   ├── fig1_a.png           # Dataset samples
│   ├── fig1_b.png
│   ├── fig2.jpg             # Model architecture
│   ├── fig3.jpg             # Adversarial training
│   ├── fig4.jpg             # Pruning process
│   ├── class_distribution_*.png
│   ├── per-class/           # Per-class performance metrics
│   │   ├── chest_xray.png
│   │   └── roct.png
│   ├── cm/                  # Confusion matrices
│   │   ├── chest_xray/      # Chest X-Ray confusion matrices
│   │   └── roct/            # ROCT confusion matrices
│   ├── asr-prunning/        # Attack success rate vs pruning
│   │   ├── chest_xray/      # Chest X-Ray ASR plots
│   │   └── roct/            # ROCT ASR plots
│   └── saliency_map/        # Saliency visualizations
│       ├── chest_xray/      # Chest X-Ray saliency maps
│       └── roct/            # ROCT saliency maps
└── ref/
    └── references.bib       # Bibliography database
```

## 🔧 Build Commands

### Main Paper Compilation

```bash
# Build main manuscript
make main
# or
make

# Build all submission documents (main + abstract + declaration)
make all
```

### Individual Document Builds

```bash
# Build abstract document
make abstract

# Build declaration of interests
make declaration-interests

# Build complete submission package
make submission-package
```

### Utility Commands

```bash
# Clean auxiliary files and rebuild everything
make clean && make all

# Validate Neurocomputing requirements
make validate

# Check page counts
make pages
```

## 📄 Document Description

- **`main.pdf`**: Complete manuscript for Neurocomputing journal submission
- **`main.tex`**: LaTeX source file with all content and formatting
- **`abstract.pdf`**: Abstract document (required for submission)
- **`abstract.tex`**: Abstract LaTeX source
- **`declaration_interests.pdf`**: Declaration of interests (required for submission)
- **`declaration_interests.tex`**: Declaration of interests LaTeX source

### Key Features

- ✅ **Elsevier Formatting**: Uses elsarticle class for Neurocomputing journal
- ✅ **Complete Visualizations**: All figures including saliency maps, confusion matrices, and performance metrics
- ✅ **Professional Formatting**: Proper citation style with numerical references
- ✅ **Comprehensive Analysis**: Attack success rate analysis, ablation studies, and per-class metrics

## 🚀 Quick Start

1. **Complete Build Workflow**:

   ```bash
   make clean && make all
   ```

2. **Individual Builds**:

   ```bash
   make main           # Build main manuscript
   make abstract       # Build abstract document
   make declaration-interests  # Build declaration of interests
   ```

3. **Development Workflow**:
   ```bash
   make clean          # Clean auxiliary files
   make main           # Build and check main document
   # Edit files as needed
   make all            # Rebuild all documents
   ```

## 📊 Document Statistics

- **Main manuscript**: ~30 pages
- **Abstract**: 1 page (required for submission)
- **Declaration of interests**: 1 page (required for submission)
- **Bibliography**: 50+ references in BibTeX format
- **Figures**: 8+ main figures + performance analysis visualizations
- **File Size**: ~8MB (due to high-quality figures)

## 📊 Data Availability

This study utilized two publicly available datasets for medical image classification tasks:

1. **Retinal OCT Images (optical coherence tomography)**  
   Available from Kermany et al. (2018) via Kaggle:  
   🔗 [https://www.kaggle.com/datasets/paultimothymooney/kermany2018](https://www.kaggle.com/datasets/paultimothymooney/kermany2018)

2. **Chest X-Ray Images (Pneumonia)**  
   Available via Kaggle:  
   🔗 [https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

### 💻 Source Code Availability

The complete implementation of the MedDef model and experimental code is available at:  
🔗 [https://github.com/Hetawk/meddef1.git](https://github.com/Hetawk/meddef1.git)

**Quick Setup:**

```bash
git clone https://github.com/Hetawk/meddef1.git
cd meddef1
# Follow setup instructions in the code repository
```

## 🔍 Technical Details

### LaTeX Packages Used

- `elsarticle`: Elsevier journal article class for Neurocomputing
- `hyperref`: PDF navigation and links
- `natbib`: Citation management with numerical style
- `subcaption`: Subfigure support
- `multirow`: Table formatting
- `graphicx`: Figure inclusion

### Build System

- **Make-based**: Uses Makefile for automated builds
- **Multi-pass**: Automatic BibTeX and cross-reference resolution
- **Clean builds**: Removes auxiliary files for fresh compilation

## 📝 File Conventions

- **Main source**: `main.tex`
- **Bibliography**: `ref/references.bib`
- **Figures**: `fig/` directory with organized subdirectories
- **Output**: `main.pdf` generated in root directory

## 🛠️ Troubleshooting

### Common Issues

1. **Compilation errors**: Run `make clean` before rebuilding
2. **Missing figures**: Ensure all figure files exist in `fig/` directory
3. **Bibliography issues**: Check `ref/references.bib` for syntax errors
4. **Memory issues**: LaTeX may need more memory for large figures

### Make Targets

```bash
make clean          # Remove auxiliary files
make main           # Build main.pdf (default target)
make               # Same as 'make main'
```

## 📚 Submission Package

For journal submission, the complete package includes:

- `main.pdf` - Complete manuscript
- `abstract.pdf` - Abstract document (required)
- `declaration_interests.pdf` - Declaration of interests (required)
- Source LaTeX files and bibliography
- All figure assets in `fig/` directory

**Build all submission documents:**

```bash
make submission-package
```

---

**Contact**: For questions about the build system or document structure, refer to the corresponding author information in the manuscript.
