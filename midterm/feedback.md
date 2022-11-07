# Notes on the Midterm

* _Correctness    (out of 40):_ 30
* _Good Practices (out of 10):_ 10
* _Docs / Testing (out of 10):_ 0

_Details on the grading criteria for the midterm can be found on [Canvas](https://canvas.slu.edu/courses/28045/rubrics/23671)._

You didn't include docstrings and tests. I've deducted 10 points from the _Docs / Testing_ category for this.

## Step 1
You had most of this right, but it was wrong enought that it wouldn't return the right answers. I deducted 5 points from _Correctness_ for this.

* Your function should open the `file` from the parameters rather than always opening the hardcoded file from `/data/negotiated_rates.json`
* Your function exists early and returns the wrong answer because your lines to compute the average rate and return it are happening deep inside your loop.  They will only get called for the first item you process and the fucntion will return right away.
* This wasn't caught because you altered the `assert` test case to incorrectly test the output.

## Step 2
* `list` is a special keyword for Python because it is global function and data type. Don't use it for a variable name.
* You've use the variable name `service_code` and `billing_code` again inside the function even though they were used as parameters. What this means is that your tests `service_code == service_code and billing_code == billing_code` will always be true on the very first try.  See how you're testing the same as `1 == 1`? I've deducted 2 points from _Correctness_ for this.

## Step 3
* You should have reused your `get_rate()` function from above instead of copying over all the same code.
* Because these test cases all use the same billing / service code combination, it didn't cause an issue for your code. You need your own testing, too.

## Step 4
* This code you wrote seems mostly reasonable, but you didn't put it into a function. I've deducted 1 points from _Correctness_ for this.
* There are quite a few other typos and errors in the code as well. I've deducted another 2 points from _Correctness_ fort them.