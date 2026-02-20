# app-plot-epochs

Brainlife App to plot average ERPs from epochs by condition using MNE-Python.

## Description

This app reads epoched MEG/EEG data and generates average ERP (Event-Related Potential) plots for each condition/event type present in the data. It creates individual plots for each condition and generates an HTML report with all visualizations included.

## Inputs

- **meg-epo.fif**: Epoched MEG/EEG data in MNE format (created by app-epoch or similar)

## Outputs

- **erp_*.png**: Individual ERP plots for each condition found in the epochs
- **report.html**: HTML report with all ERP visualizations
- **product.json**: Brainlife.io product metadata including all generated figures

## Configuration Parameters

### Required
- **epo** (string): Path to the epochs file in MNE format (*.fif)

## Features

- Automatically detects and processes all conditions/event types in the epochs
- Generates color-coded ERP plots using spatial colors
- Creates comprehensive HTML report with all plots
- Includes data statistics (number of epochs, channels, sampling rate) in product metadata
- Handles multiple conditions gracefully

## Usage

Typical workflow:
1. Create epochs using `app-epoch`
2. Run this app with the epochs file as input
3. Review the generated ERP plots and HTML report
4. Use ERPs for further analysis

## References

- [MNE-Python Documentation](https://mne.tools/)
- [Event-Related Potentials (ERPs)](https://mne.tools/stable/auto_examples/evoked/index.html)

## Authors

- Maximilien Chaumon (https://github.com/dnacombo)

## License

GPL-3.0
