### Overview
A comprehensive Python-based project for generating synthetic tabular data using statistical methods. This project creates privacy-preserving artificial datasets that mimic the statistical properties of real data while protecting sensitive information.

See the theory part of this topic.
https://medium.com/@sefabilicier/tabular-data-generation-0abf28e553e8

### Features
**Complete Data Generation**: Generate synthetic data for all column types (numerical, categorical, boolean)
**Privacy Protection**: No exact duplicates from original data
**Statistical Fidelity**: Preserves means, standard deviations, and distributions
**Quality Evaluation**: Comprehensive metrics to assess synthetic data quality
**Multiple Generation Methods**: Simple sampling, statistical models, and constraint-based generation
**Visual Analysis**: Side-by-side comparisons of original vs synthetic data

### Installation
#### Prerequisites

- Python 3.8+
- pip package manager

Setup
````bash
Please work wih the cells one by one!

````

### Step-by-Step Workflow

**Data Exploration**: Understand your data structure and distributions
**Generator Selection**: Choose appropriate generation method
**Synthetic Data Generation**: Create artificial dataset
**Quality Evaluation**: Assess statistical similarity and privacy
**Validation**: Test with downstream ML tasks


### Available Generators

**SimpleDataGenerator**
- Basic sampling with Gaussian noise
- Suitable for simple datasets
- Fast execution

````bash
generator = SimpleDataGenerator(random_state=42)
synthetic_data = generator.generate_from_data(original_data, n_samples=1000)
````
**StatisticalDataGenerator**
- Multivariate normal distribution
- Preserves correlations between numerical columns
- Better for complex datasets

**CompleteDataGenerator**
- Handles all data types
- Applies column-specific constraints
- Most comprehensive option

### Evaluation Metrics
#### Statistical Similarity
**Mean Similarity**: Comparison of column means
**Std Similarity**: Comparison of standard deviations
**Distribution Similarity**: KS test and JS divergence
**Correlation Preservation**: Pearson correlation matrices

#### Privacy Metrics
- **Exact Duplicates**: Count of identical rows
- **Uniqueness Ratio**: Percentage of unique synthetic rows
- **Statistical Distance**: Distance from original distributions

#### Utility Metrics
- **ML Compatibility**: Model performance on synthetic vs real data
- **Data Type Consistency**: Preservation of original data types
- **Constraint Satisfaction**: Adherence to business rules

### Example Results
#### Quality Score Interpretation


#### Typical Performance
- **Privacy**: 0% exact duplicates, 100% uniqueness
- **Statistical Similarity**: 85-95% similarity score
- **Generation Speed**: 1000 samples in < 1 second
