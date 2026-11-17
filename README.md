# DCIT407 Group 18: Periodic Noise Removal with Notch Filters

**Course:** DCIT407 Image Processing, Semester 1, 2026/27
**Domain:** Restoration and analysis
**Project #:** 18

## Project Overview

**What we build:** A tool that removes stripes or moiré patterns from scanned or printed images in the Fourier domain.

**Evaluation reference:** Clean original images, after adding synthetic periodic noise to them (PSNR/SSIM against the originals).

## Deliverables

- A Jupyter notebook or app
- A short report (problem, method, results, limitations)
- A 10-minute presentation in Week 13

## Course Requirements

- At least one quantitative result (PSNR/SSIM, processing time, etc.)
- A comparison of at least two methods
- 20-100 test images, each with a clean original. Dataset stated by Week 3.
- Classical methods only. A small deep-learning baseline is allowed purely as a comparison.

## Team Members and Roles

| # | Name | Student ID | Role |
|---|------|-----------|------|
| 1 | Barbara Elizabeth Korlekie Sackey | 22012722 | Project lead: coordination, deadlines, final integration |
| 2 | Boadu-Acheampong Asante Yaw | 22152286 | Dataset: collect clean images, generate synthetic periodic noise |
| 3 | Roselyn Sakyi | 22012206 | Fourier analysis: FFT, spectrum visualization, noise peak study |
| 4 | Glorious James Okyere | 22031299 | Method A: manual notch filters (ideal, Butterworth, Gaussian) |
| 5 | Lambert Klenam Nenemse | 22165472 | Method B: automatic peak detection and auto-notch |
| 6 | Thomas Theophilus Kwasi Kutin | 22045470 | Evaluation: PSNR/SSIM and processing-time code |
| 7 | Dzah Solomon Sampson Kofi | 22012447 | Experiments: parameter tuning, method comparison, real-world scans |
| 8 | Kelvin Yemoh Odoi | 22012509 | Report writing |
| 9 | Henry Ampomah | 22047836 | Presentation, plus optional demo app (Streamlit) |
| 10 | Somuah Kofi Sasu | 22061652 | Testing, code cleanup, documentation, limitations |

> Roles are a starting point and can be swapped to suit members' skills.

---

## Milestones and Tasks

### Week 3: Topic approval and dataset stated

- [ ] **Barbara:** Set up the shared repo and chat group; submit the topic and dataset statement.
- [ ] **Boadu-Acheampong:** Gather 20-100 clean images (documents, photos, scans); record the source and licence.
- [ ] **Roselyn:** Review the theory (FFT, centred spectrum, how stripes and moiré appear as spikes).
- [ ] **Glorious and Lambert:** Read up on notch filter types and peak detection; shortlist the two methods to compare.
- [ ] **Thomas:** Decide the evaluation metrics (PSNR, SSIM, time).
- [ ] **Dzah, Kelvin, Henry, Somuah:** Check dataset quality; draft the report outline and a task tracker.

### Week 7: Working first pipeline

- [ ] **Boadu-Acheampong:** Finish the noise generator (sinusoidal stripes at different frequencies and angles, moiré-like patterns); save noisy and clean pairs.
- [ ] **Roselyn:** Build the FFT, spectrum display and inverse FFT module.
- [ ] **Glorious:** Implement manual notch filtering, with at least one filter type working end to end.
- [ ] **Lambert:** Implement a first version of automatic peak detection.
- [ ] **Thomas:** Write the PSNR/SSIM function and a loop to run it over all image pairs.
- [ ] **Dzah:** Test the first pipeline on a few images and log problems.
- [ ] **Barbara:** Merge everything into one notebook; review the code.
- [ ] **Kelvin:** Start the report (problem statement, introduction, method).
- [ ] **Henry:** Start the slide template; sketch the demo app layout.
- [ ] **Somuah:** Write the README details and make sure the code runs from scratch.

### Week 11: Results with evaluation

- [ ] **Glorious:** Complete the ideal, Butterworth and Gaussian filters; tune radius and order.
- [ ] **Lambert:** Finish the automatic method; measure peak detection quality and any removal of real image content.
- [ ] **Dzah:** Run the full comparison (at least two methods across all noise types); try a few real scanned or printed images.
- [ ] **Thomas:** Produce results tables, charts and processing times.
- [ ] **Roselyn:** Make before/after spectrum figures for the report.
- [ ] **Boadu-Acheampong:** Add harder cases (multiple frequencies, stronger noise); confirm the references are correct.
- [ ] **Kelvin:** Write the results and limitations sections.
- [ ] **Somuah:** Check reproducibility, fix bugs and compile the limitations list.
- [ ] **Henry:** Build the slides with results, plus the demo app if included.
- [ ] **Barbara:** Review the draft report and results against the course requirements (one quantitative result, two methods compared).

### Week 13: Mini project presentation (10% of course grade)

- [ ] **Henry and Barbara:** Finalize slides and run timed rehearsals.
- [ ] **Kelvin and Somuah:** Polish and proofread the report; package the notebook, report and slides.
- [ ] **Glorious and Lambert:** Present the methods.
- [ ] **Roselyn and Boadu-Acheampong:** Present the problem, data and noise.
- [ ] **Thomas and Dzah:** Present results and comparison.
- [ ] **Henry and Barbara:** Intro, conclusion and demo.

> The presentation is only 10 minutes, so consider narrowing the speakers to 4-5 people, with the rest as backup for questions.

---

## Suggested Methods to Compare

- Ideal vs Butterworth vs Gaussian notch filters
- Manual vs automatic peak detection in the Fourier spectrum

## Suggested Repository Structure

```
.
├── README.md
├── data/
│   ├── clean/          # original images
│   └── noisy/          # images with synthetic periodic noise
├── notebooks/
│   └── pipeline.ipynb
├── src/
│   ├── noise.py        # noise generation
│   ├── fourier.py      # FFT utilities
│   ├── filters.py      # notch filters
│   ├── detect.py       # automatic peak detection
│   └── metrics.py      # PSNR, SSIM, timing
├── results/            # tables and figures
├── report/
└── slides/
```
