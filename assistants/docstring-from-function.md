# LLM Instruction: Generate Standardized Function Docstrings

## Task
Given a function, generate a comprehensive docstring following Google-style format and Python documentation best practices.

## Format Requirements
Use Google-style docstrings with the following structure:

```python
def function_name():
    """Brief one-line summary ending with a period.
    
    Optional longer description providing more context, use cases, 
    or implementation details. This can span multiple paragraphs.
    
    Args:
        param_name (type): Description of parameter. Include constraints,
            valid ranges, or expected formats.
        optional_param (type, optional): Description. Defaults to value.
    
    Returns:
        type: Description of return value. Be specific about the type
            and structure of returned data.
    
    Raises:
        ExceptionType: Description of when this exception is raised.
        AnotherException: Description of another potential exception.
    
    Example:
        Basic usage example:
        
        >>> result = function_name(arg1, arg2)
        >>> print(result)
        Expected output
        
        More complex example if needed:
        
        >>> # Setup code
        >>> advanced_result = function_name(complex_arg)
        >>> assert advanced_result.property == expected_value
    
    Note:
        Any important implementation details, performance considerations,
        or usage warnings.
    """
```

## Content Guidelines

### Summary Line
- Start with a verb in imperative mood ("Calculate", "Return", "Process")
- Be concise but descriptive (under 80 characters)
- End with a period
- Avoid redundant phrases like "This function..."

### Extended Description
- Explain the purpose and behavior
- Describe the algorithm or approach if complex
- Mention use cases or context where applicable
- Keep paragraphs focused and well-organized

### Parameters (Args)
- Include type hints in parentheses
- Use "optional" for parameters with defaults
- Specify valid ranges, formats, or constraints
- Mention units for numerical parameters
- Use consistent parameter names with function signature

### Return Values
- Always specify the return type
- Describe the structure for complex returns (dicts, tuples, objects)
- Explain what the return value represents
- For generators/iterators, describe what each yielded item contains

### Exceptions
- Document all exceptions the function might raise
- Include both direct raises and common exceptions from dependencies
- Explain the conditions that trigger each exception

### Examples
- Provide at least one working example
- Use realistic, meaningful data
- Show expected output where helpful
- Include edge cases for complex functions
- Use doctest format for testable examples

### Additional Sections (when relevant)
- **Note**: Important implementation details or warnings
- **See Also**: References to related functions
- **References**: Citations for algorithms or external sources

## Quality Standards
- Write in present tense, third person
- Use clear, concise language
- Avoid jargon unless necessary (then define it)
- Be consistent with terminology throughout
- Ensure examples are copy-pasteable and runnable
- Match the technical level to the intended audience

## Example Output

```python
def calculate_compound_interest(principal, rate, time, compounds_per_year=1):
    """Calculate compound interest for a given principal amount.
    
    Computes the final amount after compound interest is applied over
    a specified time period. Uses the standard compound interest formula:
    A = P(1 + r/n)^(nt), where A is the final amount.
    
    Args:
        principal (float): Initial principal amount in dollars. Must be positive.
        rate (float): Annual interest rate as a decimal (e.g., 0.05 for 5%).
            Must be between 0 and 1.
        time (int): Time period in years. Must be positive.
        compounds_per_year (int, optional): Number of times interest compounds
            per year. Common values are 1 (annually), 4 (quarterly), 
            12 (monthly), 365 (daily). Defaults to 1.
    
    Returns:
        float: Final amount after compound interest, rounded to 2 decimal places.
    
    Raises:
        ValueError: If principal, rate, or time are negative, or if 
            compounds_per_year is less than 1.
        TypeError: If any argument is not a number.
    
    Example:
        Calculate interest on $1000 at 5% for 3 years:
        
        >>> amount = calculate_compound_interest(1000, 0.05, 3)
        >>> print(f"${amount:.2f}")
        $1157.63
        
        Monthly compounding:
        
        >>> amount = calculate_compound_interest(1000, 0.05, 3, 12)
        >>> print(f"${amount:.2f}")
        $1161.62
    
    Note:
        Result is rounded to 2 decimal places for currency representation.
        For high-precision calculations, consider using the decimal module.
    """
```

## Instructions for Implementation
1. Analyze the function signature, body, and context
2. Identify the primary purpose and behavior
3. Determine all parameters, their types, and constraints
4. Identify return type and structure
5. Consider potential exceptions
6. Create realistic, useful examples
7. Write clear, professional documentation following the format above
