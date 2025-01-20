# topsis-102203846
A Python package for implementing the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) decision-making algorithm.

## Installation

Install the package using pip:

```bash
pip install topsis-102203846
```

## Usage

You can use this package from the command line to perform TOPSIS calculations.

### Command-Line Usage

```bash
python <RollNumber>.py <InputDataFile> <Weights> <Impacts> <ResultFileName>
```

#### Arguments:
1. **InputDataFile**: Path to the input CSV file containing the decision matrix.
2. **Weights**: Comma-separated list of weights for each criterion (e.g., `1,1,1,2`).
3. **Impacts**: Comma-separated list of impacts for each criterion (`+` for beneficial, `-` for non-beneficial).
4. **ResultFileName**: Path to save the result CSV file with TOPSIS scores and ranks.

### Example

```bash
python 12345.py data.csv "1,1,1,2" "+,+,-,+" result.csv
```

### Input File Format

The input file must be a CSV with:
- At least three columns.
- The first column containing object names (e.g., `M1`, `M2`).
- The remaining columns containing numeric values.

#### Example Input File (`data.csv`):

| Object | f1  | f2  | f3  | f4  |
|--------|-----|-----|-----|-----|
| M1     | 250 | 16  | 12  | 8   |
| M2     | 200 | 12  | 8   | 6   |
| M3     | 300 | 18  | 14  | 10  |
| M4     | 275 | 14  | 10  | 7   |

### Output File Format

The output file contains the input data along with two additional columns:
- **Topsis Score**: The computed TOPSIS score for each object.
- **Rank**: The rank based on the TOPSIS score.

#### Example Output File (`result.csv`):

| Object | f1  | f2  | f3  | f4  | Topsis Score | Rank |
|--------|-----|-----|-----|-----|--------------|------|
| M1     | 250 | 16  | 12  | 8   | 0.5674       | 2    |
| M2     | 200 | 12  | 8   | 6   | 0.3412       | 4    |
| M3     | 300 | 18  | 14  | 10  | 0.6789       | 1    |
| M4     | 275 | 14  | 10  | 7   | 0.4532       | 3    |

## Requirements

- Python 3.6 or higher
- pandas
- numpy

Install dependencies with:

```bash
pip install -r requirements.txt
```


## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Author

- **Aditi Sinha**
- Roll Number: 102203846
