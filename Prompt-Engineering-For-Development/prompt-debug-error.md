1. **Error Details**:
   - Error message: `AttributeError: 'NoneType' object has no attribute 'split'`
   - Full traceback:

     ```
     Traceback (most recent call last):
       File "example.py", line 12, in <module>
         result = process_data(data)
       File "example.py", line 8, in process_data
         return data.split(',')
     AttributeError: 'NoneType' object has no attribute 'split'
     ```

   - The error occurs when calling the `process_data` function with a `None` input.

2. **Code Context**:
   - Relevant code:

     ```python
     def process_data(data):
         return data.split(',')
     ```

   - Recent changes: The function was modified yesterday to handle CSV data.

3. **Environment Information**:
   - Python version: 3.9.7
   - Operating system: macOS 12.0
   - Dependencies: `pandas==1.3.3`, `numpy==1.21.2`
   - Using `venv` for the virtual environment.

4. **Steps to Reproduce**:
   - Call `process_data(None)` in the code or pass `None` as input to the function.

5. **Expected vs. Actual Behavior**:
   - Expected: The function should handle `None` input gracefully or raise a meaningful error.
   - Actual: The function crashes with an `AttributeError`.

6. **Debugging Attempts**:
   - Added a print statement to check the input: `print(f"Data: {data}")`, which confirmed `data` is `None`.
   - Tried adding a check for `None` but unsure how to proceed.

7. **Additional Context**:
   - The function is part of a data processing pipeline that reads data from a CSV file. Sometimes the file is empty, leading to `None` input.
