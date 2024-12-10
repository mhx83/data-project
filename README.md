# Monthly Cost Report Generator

## **How to Run**
1. **Install**: Ensure Python 3.7+ is installed. No additional dependencies are required.
2. **Run the Script**:
   ```bash
   python monthly_cost_report.py <input_file> <output_file>
   ```
   Example:
   ```bash
   python monthly_cost_report.py billing_log_small.txt cost_report_small.txt
   ```

---

## **Design Decisions**
- **Data Structures**:
  - `list`: To maintain the order of members and providers as declared.
  - `defaultdict`: For grouping bills by month and aggregating totals.
- **Sorting**: Dates are grouped and sorted using `"%Y-%m"` format to ensure chronological order.
- **Output Format**: Members and providers are listed by declaration order, adhering to the requirements.

---

## **How to Test**
1. Run the tests with:
   ```bash
   python -m unittest test_monthly_cost_report.py
   ```
2. **Test Cases**:
   - **Correctness**: Compare generated reports with expected outputs for small, medium, and large inputs.
   - **Performance**: Ensure xlarge input runs in under 60 seconds.
