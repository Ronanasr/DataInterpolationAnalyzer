# DataInterpolationAnalyzer

## Description
This Python script reads x-y data from a text file, performs linear interpolation to create a smooth curve, computes the numerical derivative, and visualizes both the interpolated function and its derivative. It leverages `numpy` for efficient computations and `matplotlib` for plotting. The script generates two high-quality plots: one for the original and interpolated data, and another for the numerical derivative, both saved as PNG images.

## Features
- Reads x-y data from a text file.
- Performs linear interpolation using `numpy.interp` for a smooth curve.
- Computes the numerical derivative using `numpy.gradient` for accuracy.
- Generates and saves two plots: interpolated data and numerical derivative.
- Includes error handling for file input and data processing.
- Customizable plot settings (size, resolution, and number of interpolation points).

## Requirements
- Python 3.x
- Required libraries:
  - `numpy`
  - `matplotlib`

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/data-interpolation-analyzer.git
   ```
2. Navigate to the project directory:
   ```bash
   cd data-interpolation-analyzer
   ```
3. Install the required libraries:
   ```bash
   pip install numpy matplotlib
   ```

## Usage
1. Prepare a text file (e.g., `data-der.txt`) with two columns: x and y values, separated by whitespace.
2. Save the script as `interpolation_derivative.py`.
3. Run the script:
   ```bash
   python interpolation_derivative.py
   ```
4. The script will:
   - Generate two plots:
     - Interpolated data with original points (`interpolation_plot.png`).
     - Numerical derivative of the interpolated function (`derivative_plot.png`).
   - Save both plots in the project directory.
   - Display the plots (optional; can be disabled by commenting out `plt.show()`).

## Example Output
Below are example plots generated from a sample dataset:

**Interpolated Data**:
![Interpolation Plot](interpolation_plot.png)

## Code Explanation
- **Function**: `plot_interpolation_and_derivative(file_path, num_points=500, figsize=(8, 6), dpi=300)`
  - Reads data from a specified file and validates its existence.
  - Performs linear interpolation using `numpy.interp` to create a smooth curve.
  - Computes the numerical derivative using `numpy.gradient` for improved accuracy.
  - Generates two plots with customizable settings (figure size, resolution, etc.).
  - Saves plots as `interpolation_plot.png` and `derivative_plot.png`.
- **Key Parameters**:
  - `file_path`: Path to the input data file (e.g., `data-der.txt`).
  - `num_points = 500`: Number of points for interpolation.
  - `figsize = (8, 6)`: Size of the plot figures.
  - `dpi = 300`: Resolution for saved plots.

## Input File Format
The input file (e.g., `data-der.txt`) should contain two columns:
- First column: x values (independent variable).
- Second column: y values (dependent variable).
- Values should be separated by whitespace.

Example `data-der.txt`:
```
0.0 0.0
1.0 1.0
2.0 4.0
3.0 9.0
```

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or feedback, feel free to open an issue on GitHub or contact [ronasr82@gmail.com](mailto:ronasr82@gmail.com).
