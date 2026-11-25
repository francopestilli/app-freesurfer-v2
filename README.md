# recon-all-for-meeeg

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Runs FreeSurfer 7.1.1 recon-all on a T1-weighted image to produce cortical surfaces and segmentation for MEG/EEG coregistration and BEM creation.**

Runs the full FreeSurfer recon-all pipeline (-all, parallel, 8 OpenMP threads) on the T1w image and outputs the subject directory. It is meant as the anatomy step of MEG/EEG pipelines, feeding coregistration and BEM Apps. No options are exposed (no hires, T2 or expert settings); expect many hours of compute and a FREESURFER_LICENSE or FS_LICENSE on the resource. The repository has no README.

| | |
|---|---|
| 📥 **Inputs** | `neuro/anat/t1w` |
| 📤 **Outputs** | `neuro/freesurfer` |
| 🐳 **Container** | `brainlife/freesurfer:7.1.1` |
| ⚙️ **Resources** | 8 CPUs · 40 GB memory · 20 h walltime |
| 🔑 **Requires** | `FREESURFER_LICENSE`, `FS_LICENSE` |
| 🔗 **Run it** | [doi.org/10.25663/brainlife.app.898](https://doi.org/10.25663/brainlife.app.898) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `t1` | `neuro/anat/t1w` | yes | T1-weighted anatomical MRI for FreeSurfer recon-all surface reconstruction |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `output` | `neuro/freesurfer` | FreeSurfer recon-all output containing cortical surfaces and segmentation. Used as input for coregistration (app-coreg) and BEM model creation (app-bem). |

<!-- brainlife-app:end -->

