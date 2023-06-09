<a alt="NHS-R Community's logo" href='https://nhsrcommunity.com/'><img src='https://nhs-r-community.github.io/assets/logo/nhsr-logo.png' align="right" height="80" /></a>

# Quarto Report NHS Theme

## About

An NHS theme for Quarto `.html` reports

_**Note:** No data, public or private are shared in this repository._

## Getting Started

Quarto is a powerful system for creating reports, presentations, and interactive applications using a wide range of formats. This user guide will walk you through the process of applying the NHS report theme to a Quarto report in R-Studio, giving your report a professional, consistent look in line with the NHS branding guidelines.

### Table of Contents

1. [Prerequisites](#prerequisites)
2. [Set the YAML options](#yaml-options)
3. [Render the Quarto report](#render-report)
4. [Troubleshooting](#troubleshooting)
5. [Example Report](#example)

<a name="prerequisites"></a>

### 1. Prerequisites

To follow this guide, you will need the following:

- A working installation of Quarto (install from https://quarto.org)
- R-Studio installed on your computer (install from https://www.rstudio.com)
- The example [Quarto report template](/report_template.qmd) (`.qmd` file)
- The [NHS report theme](/NHS_report_theme.css) (`.css` file)

<a name="yaml-options"></a>

### 2. Set the Report YAML options

In order to apply the NHS report theme to your Quarto report, you will need to update the YAML metadata at the beginning of your `.qmd` file. Follow these steps:

- Open your [Quarto report template](/report_template.qmd) in R-Studio.
- Locate the YAML metadata section at the beginning of the file, enclosed by `---` lines.
- Add the `css` option under the `html` output format, and set its value to the path of the [NHS report theme](/NHS_report_theme.css).

```yaml
---
title: "My Quarto Report"
author: "John Doe"
output:
  html_document:
    css: "/NHS_report_theme.css"
---
```

**Note** Make sure to use the correct file path. Should be relative to the root of the project folder.

- If you are makeing an [embedded report](https://quarto.org/docs/output-formats/html-publishing.html#standalone-html) to email out, add the `self_contained` option under the `html` output format, and set its value to `true`:

```yaml
---
title: "My Quarto Report"
author: "John Doe"
output:
  html_document:
    css: "path/to/nhs-theme.css"
    self_contained: true
---
```

There are many other options in the template YAML file that set the look and functionality of the output, you can lookup each option in the [Quarto docs](https://quarto.org/docs/output-formats/html-basics.html).

<a name="render-report"></a>

### 3. Render the Quarto report

With the YAML options updated, you can now render the Quarto report with the NHS R report theme applied. Follow these steps:

- In R-Studio, with your [Quarto report template](/report_template.qmd) open, click on the 'Render' button located in the toolbar.
- R-Studio will render the Quarto report and display the output in a new browser window, with the NHS R report theme applied.
- The rendered [report_template.html](/report_template.html) file will be saved in the same folder within the report directory.

<a name="troubleshooting"></a>

### 4. Troubleshooting

If you encounter any issues during the rendering process or with the appearance of the NHS theme in your Quarto report, consider the following:

- Check the file path of the NHS report theme in the YAML metadata to ensure it is correct.
- Ensure that the NHS report theme file is [properly formatted](https://quarto.org/docs/output-formats/html-themes.html#theme-options) and does not contain any syntax errors.
- Consult the Quarto documentation (https://quarto.org/docs/) for additional guidance and troubleshooting tips.

<a name="example"></a>

### 5. NHS England Example Report

An example report developed by the NHS England R community has been provided that uses the quarto-nhs-report-theme: [example_AE_report](/example_AE_report.qmd). 
The report shows how the NHS theme can be used to develop open-source analytical reports using R and Quarto and can be previewed at [https://nhsengland.github.io/nhs-r-reporting/examples/ae_attendance.html](https://nhsengland.github.io/nhs-r-reporting/examples/ae_attendance.html)

## Contributing

Please see our [guidance on how to contribute](https://tools.nhsrcommunity.com/contribution.html).

This project is released with a Contributor [Code of Conduct](./CODE_OF_CONDUCT.md). 
By contributing to this project, you agree to abide by its terms.

## Roadmap

See the [open issues](https://github.com/nhs-r-community/quarto-nhs-theme/issues) for a list of proposed features (and known issues).

## License

Distributed under a MIT Licence. _See [LICENCE.md](/LICENCE) for more information._
