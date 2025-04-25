---
title: "Introduction to Unit Testing with Python"
date: 2025-04-11T14:58:32+01:00
draft: false
ShowLastMod: true
summary: The first in a series of tutorials about testing in Python
---

## Why test?

It may sound boring, but tests keep the world in check. They help us diagnose issues, understand things and prevent failure.

Tests are also not just a ‘software’ thing. They are used in so many industries across the world:

- Chemistry: A “Litmus test” tests materials for their pH level
- Medicine: A “blood test” tests for all kinds of information
- Electrician: A “socket test” tests that an electrical socket is safe to use
- Banking: A “stress test” tests that a bank can withstand an economic shock

_Have a think about your current job or field of study, what tests can you think of? Let me know in the comments!_

When you’re writing code that you want to be confident that it is doing what you think it is. This is why we test.

## Testing Tutorial

### 1. Write Your Function

Before I walkthrough the basics of testing in Python, I will setup the function that we want to test. For the purposes of the tutorial, it is kept very simple, but the steps can be replicated to test much more complex functions as you grow as a Pythonista!

```python

def cube(a):
    """
    Returns the result of: a * a * a
    i.e. the cube of value a (a^3)
    """

    return a * a * a
```

The code above represents our python file `some_maths.py`. We’ve defined a function `cube()` that takes a number, and returns its cube value.

For example: 2 cubed is 8; 3 cubed is 27.

### 2. Install pytest

Ensure that `pytest` is installed in your preferred environment (`poetry`, `uv`, `conda`, `venv` etc.).

### 3. Create a test file

Once we have written our function, we can now test it. We will make use of a common Python library called `pytest`. It is one of the most commonly used Python libraries for testing code, and I highly recommend it.

![unit_testing](/images/unit_testing_1.png)

A crucial thing to know when writing tests for your python code, is that the test file, must be prefixed with `test_`. This is linked to how pytest _discovers_ where your tests are in your directory. As you can see in my example pictured above, I have my function contained in `somemaths.py` and then my test is in a file called `test_some_maths.py`.

### 4. Write your test

When writing a test, I have learnt a common structure called **AAA** -> Assemble, Act, Assert.

1. Assemble: Get all your inputs and variables setup
2. Act: Run the code you want to test and capture the results
3. Assert: Assert the results equal what you expected

```python
from some_maths import cube


def test_cube_fn_is_correct():
    """
    Test that the `cube()` returns the correct result!
    """

    # Define the inputs
    input_value = 3

    # Define what you expect to happen
    expected_result = 27

    # Run the function
    result = cube(input_value)

    # Verify that the result, is what you expected
    assert result == expected_result

```

Firstly, we import the code we want to test. So we run: `from some_maths import cube`.

We then proceed to write out test for the `cube()` function. Note again that the test
follows the pattern of being prefixed with `test_`. This is for the same reason we named
our test file, it is linked to how pytest discovers the tests in our directories.

We set the `input_value` to `3`, and armed with our knowledge of maths,
we know the result of 3 cubed should be `27`.

We then run this function and capture the result.

Finally, we use the builtin Python keyword `assert` to verify the result is what we expected.
If the result is 27, as we expected, we are asserting 27 equals 27, and therefore our assertion becomes `True`
and the test will pass!

### 5. Run the test (and hopefully, they pass!)

Once the test is written, we can now use it to see if our code works.

To do this, open up your command line (console/terminal/shell) and navigate to your project directory. Then you can type in: `pytest test_some_maths.py `

If you’ve followed along, you should see something like the below. It begins the test (“test session starts”), it finds 1 test (“collected 1 item”), and then tells you the results (“1 passed in 0.01s”).

![unit_testing](/images/unit_testing_2.png)

## What's next?

There is so much more to learn about testing practices. Such as:

- Parametrization
- Mocking & Patching
- Fixtures
- Integration Testing

Look out for more posts where I will provide overviews and tutorials of those testing concepts!
