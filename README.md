- This project investigates whether machine learning applied to FTIR imaging data can improve the early classification of oral epithelial lesions as benign or malignant. 
- The key aim was to determine whether equivalent diagnostic performance could be achieved using standard glass slides, rather than calcium fluoride substrates, to reduce barriers to clinical adoption. 
- The work combines spectral preprocessing, supervised neural networks, and statistical evaluation on biopsy-level held-out data.

## Summary (non-technical) of the project:
This project explores a way to help clinical professionals treat 
oral cancers more accurately, and hopefully with fewer painful repeat biopsies, by using imaging
techniques and artificial intelligence. Currently, tissue samples are examined under a microscope by
a histopathologist (someone who studies changes in tissues caused by disease), but studies show they
can only predict which early lesions will turn cancerous (since they with either remain benign or
become cancerous) about 25–40% of the time. When imaged using infrared techniques, very small
differences in the spectra can reveal the chemistry inside each cell. Many of these spectra are fed
into a simple neural network “brain” (called a multi-layer perceptron) that learns to tell benign from
malignant tissue. Even without access to the region of the spectrum which calcium fluoride allows
us to see (calcium fluoride is not currently used in clinical practice but it allows us to see a region
of the spectrum called the fingerprint band, which provides the artificial intelligence with much
more information), the method on glass slides already used in the clinic (where we can no longer
access the information-rich fingerprint region) achieves∼99% accuracy at spotting healthy tissue
and 77% accuracy at identifying cancerous changes. In tests on biopsies unseen to the algorithm, it
can also highlight potentially cancerous regions the pathologist missed. These results suggest that
combining infrared imaging techniques with machine learning could give patients clearer answers
faster and significantly improve their outcomes and experience.


## Dissertation Abstract (technical):
Accurate classification of oral epithelial lesions into benign tumour and malignant tumour categories
is critical for timely diagnosis and improved patient outcomes. Currently, in the clinic, a predictive
power for malignancy in these biopsies of 25-40% is seen when a histopathologist alone examines the
biopsy. As a result, patients must attend painful biopsy procedures year-on-year when the statistics
show that only 1 in 8 will become malignant. Fourier transform infrared (FTIR) imaging offers an
alternative and potentially very powerful approach to characterising tissue. The fingerprint band
(the wavenumber range from 1000–1800 cm−1) of the FTIR spectrum is currently used in such
studies, using tissue samples mounted on CaF2 slides as standard microscope glass slides absorb
strongly in the fingerprint band. This project investigates whether the functional band (from 2200
to 4000 cm−1) accessible using glass slides, allows lesion classification as reliable as that obtainable
using CaF2. This project used FTIR data from 17 oral biopsies (10 malignant and 7 benign), and
trained a multi-layer perceptron (MLP) on pixel-level spectra. On unseen data, the functional
band achieved 99% ±0.4% specificity and 77% ±5.5% sensitivity (95% CI), compared to 99% ±
0.6% specificity and 89% ±3.1% sensitivity when the fingerprint band is used, demonstrating only
a modest performance trade-off. This is a significant performance improvement from the current
ability of a histopathologist to predict the progression of the lesion (22%-40% accuracy). When
tests were carried out using biopsies that were not represented in the training sample, for many
samples the performance was similar to that using unseen data of samples that were present in
the training dataset, though this was not the case for all unrepresented samples: further study is
required here. It has also been shown for the first time that an MLP can select malignant regions
beyond those identified by the histopathologist, a finding supported using unsupervised k-means
clustering. These may represent areas where the additional information provided by the IR spectra
allow improvements over purely manual annotation. Achieving near-equivalent classification using
glass slides rather than CaF2 simplifies the introduction of FTIR-based techniques in the existing
histopathology workflow, facilitating clinical (and commercial) adoption and potentially reducing
the number of painful biopsies patients with oral lesions must undergo while improving the accuracy
of diagnoses.


## Methods (high level)

- FTIR hyperspectral imaging of 17 oral biopsies (benign and malignant samples).
- Spectral preprocessing and normalisation (global product, local difference, local ratio).
- Supervised classification using a multi-layer perceptron (MLP).
- Biopsy-level train/test splits to assess generalisation.
- Statistical evaluation using sensitivity, specificity, and confidence intervals.
- Comparison with unsupervised k-means clustering for validation.

## Full dissertation
The complete dissertation (including methodology, results, and discussion) is available as a PDF in this repository.


