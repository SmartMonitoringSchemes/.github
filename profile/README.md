# Welcome! :wave:

<img src="/images/overlay.png" align="left" width="180" alt="Overlay">

This organization contains the code to reproduce the figures and the results of my PhD thesis titled "[Robust Modelling of Internet Delay and Smart Monitoring Schemes for the Automation of Overlay Networks](https://tel.archives-ouvertes.fr/tel-03666771/document)" (2020).

The datasets used can be downloaded on [Zenodo](https://zenodo.org/record/7035667). These datasets are compiled from public sources ([CAIDA MANIC](https://www.caida.org/projects/manic/), [RIPE Atlas](https://atlas.ripe.net)).

Feel free to contact me if you have any questions; my main GitHub account is [@maxmouchet](https://github.com/maxmouchet) and my email address is max@maxmouchet.com.

<br/>

## Repositories

### Analysis and Simulations

These repositories contains code and notebooks used to analyze datasets and perform simulations.  
The tables and figures in my PhD thesis are generated in these repositories.

Repository | Language(s) | Tests | Coverage
-----------|-------------|-------|--------
[LargeScaleAnalysis](https://github.com/SmartMonitoringSchemes/LargeScaleAnalysis) | Julia | [![CI](https://img.shields.io/github/actions/workflow/status/SmartMonitoringSchemes/LargeScaleAnalysis/tests.yml?logo=github&label=tests)](https://github.com/SmartMonitoringSchemes/LargeScaleAnalysis/actions/workflows/tests.yml) | [![codecov](https://img.shields.io/codecov/c/github/SmartMonitoringSchemes/LargeScaleAnalysis?logo=codecov&logoColor=white)](https://app.codecov.io/gh/SmartMonitoringSchemes/LargeScaleAnalysis)
[ModelComparison](https://github.com/SmartMonitoringSchemes/ModelComparison) | Julia, Python | [![CI](https://img.shields.io/github/actions/workflow/status/SmartMonitoringSchemes/ModelComparison/tests.yml?logo=github&label=tests)](https://github.com/SmartMonitoringSchemes/ModelComparison/actions/workflows/tests.yml) | [![codecov](https://img.shields.io/codecov/c/github/SmartMonitoringSchemes/ModelComparison?logo=codecov&logoColor=white)](https://app.codecov.io/gh/SmartMonitoringSchemes/ModelComparison)
[ParsimoniousMonitoring](https://github.com/SmartMonitoringSchemes/ParsimoniousMonitoring) | Julia | [![CI](https://img.shields.io/github/actions/workflow/status/SmartMonitoringSchemes/ParsimoniousMonitoring/tests.yml?logo=github&label=tests)](https://github.com/SmartMonitoringSchemes/ParsimoniousMonitoring/actions/workflows/tests.yml) | [![codecov](https://img.shields.io/codecov/c/github/SmartMonitoringSchemes/ParsimoniousMonitoring?logo=codecov&logoColor=white)](https://app.codecov.io/gh/SmartMonitoringSchemes/ParsimoniousMonitoring)
[Shao17](https://github.com/SmartMonitoringSchemes/Shao17) | Julia, Python, R | [![CI](https://img.shields.io/github/actions/workflow/status/SmartMonitoringSchemes/Shao17/tests.yml?logo=github&label=tests)](https://github.com/SmartMonitoringSchemes/Shao17/actions/workflows/tests.yml) | [![codecov](https://img.shields.io/codecov/c/github/SmartMonitoringSchemes/Shao17?logo=codecov&logoColor=white)](https://app.codecov.io/gh/SmartMonitoringSchemes/Shao17)

### Tools and Libraries

These repositories contains libraries that can be re-used in other projects.  
The Julia libraries are registered in the [SmartMonitoringSchemes/Registry](https://github.com/SmartMonitoringSchemes/Registry) repository.

Repository | Language(s) | Tests | Coverage | Documentation
-----------|-------------|-------|----------|--------------
[fetchmesh](https://github.com/SmartMonitoringSchemes/fetchmesh) | Python | [![CI](https://img.shields.io/github/actions/workflow/status/SmartMonitoringSchemes/fetchmesh/tests.yml?logo=github&label=tests)](https://github.com/SmartMonitoringSchemes/fetchmesh/actions/workflows/tests.yml) | [![codecov](https://img.shields.io/codecov/c/github/SmartMonitoringSchemes/fetchmesh?logo=codecov&logoColor=white)](https://app.codecov.io/gh/SmartMonitoringSchemes/fetchmesh) | [![Documentation](https://img.shields.io/badge/documentation-pdf-blue.svg?logo=read-the-docs&logoColor=white)](https://github.com/SmartMonitoringSchemes/fetchmesh/raw/gh-pages/fetchmesh.pdf)
[HDPHMM.jl](https://github.com/SmartMonitoringSchemes/HDPHMM.jl) | Julia | [![CI](https://img.shields.io/github/actions/workflow/status/SmartMonitoringSchemes/HDPHMM.jl/tests.yml?logo=github&label=tests)](https://github.com/SmartMonitoringSchemes/HDPHMM.jl/actions/workflows/tests.yml) | [![codecov](https://img.shields.io/codecov/c/github/SmartMonitoringSchemes/HDPHMM.jl?logo=codecov&logoColor=white)](https://app.codecov.io/gh/SmartMonitoringSchemes/HDPHMM.jl) | See the [tests](https://github.com/SmartMonitoringSchemes/HDPHMM.jl/tree/master/test)
[ThesisTools](https://github.com/SmartMonitoringSchemes/ThesisTools) | Julia, Python | [![CI](https://img.shields.io/github/actions/workflow/status/SmartMonitoringSchemes/ThesisTools/tests.yml?logo=github&label=tests)](https://github.com/SmartMonitoringSchemes/ThesisTools/actions/workflows/tests.yml) | [![codecov](https://img.shields.io/codecov/c/github/SmartMonitoringSchemes/ThesisTools?logo=codecov&logoColor=white)](https://app.codecov.io/gh/SmartMonitoringSchemes/ThesisTools) | N/A

## Usage

The minimal requirements for using the code provided in the repositories are as follow:
- Python 3.7+
- Julia 1.4+
- (Optional) IPython and IJulia, for running the notebooks
- (Optional) [tikzplotlib](https://github.com/nschloe/tikzplotlib) for producing some of the plots

### Setup

```bash
# Verify Python and Julia versions
pip --version    # pip 20.1.1 from ... (python 3.7)
python --version # Python 3.7.6
julia --version  # julia version 1.5.0

# Install the optional dependencies
pip install ipython jupyterlab tikzplotlib
julia -e 'using Pkg; Pkg.add("IJulia")'
```

In addition, the [JuliaPOMDP/Registry](https://github.com/JuliaPOMDP/Registry) and the [SmartMonitoringSchemes/Registry](https://github.com/SmartMonitoringSchemes/Registry) registries are required:
```julia
# Run the following in a Julia REPL
using Pkg
pkg"registry add General"
pkg"registry add https://github.com/JuliaPOMDP/Registry"
pkg"registry add https://github.com/SmartMonitoringSchemes/Registry"
```

### General layout

Analysis and simulations repositories follows a layout similar to this one:
```bash
data/       # Small, usually textual, input files. Larger files are stored on backup1.enstb.org.
figures/    # PDF figures
notebooks/  # Notebooks, where the plots and results are generated
plots/      # TikZ (LaTeX) figures
results/    # Results, usually CSV files
scripts/    # Scripts for long running computations
src/        # Code common to the notebooks and the scripts
test/       # Unit tests for the common code
```

### Reproducing the results

```bash
# Clone the repository, for example with the Shao17 repository:
git clone git@github.com:SmartMonitoringSchemes/Shao17.git
cd Shao17/

# Instantiate the notebooks dependencies
julia --project=notebooks/ -e 'using Pkg; pkg"instantiate"'

# Run Jupyter
jupyter lab
```

