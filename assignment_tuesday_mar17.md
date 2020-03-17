#
# Tuesday, March 17, 2020


Today's assignment will consist of one reading assignment and one coding assignment

# I. Reading
Read the rest of Chapter 6; do the quiz at the end. That will be pages 186-193.
Then answer the following questions:
1. Explain in 2 or more sentences, what a shared reference is. Give an example.
2. What is an 'in place' change to an object? What is the alternative to doing an 'in place' change?
Why is this significant?
3. Let's say we have a list = [1,2,3]. Give an example of an 'in place' and a non-'in place' change to this list.


# II. Coding exercise.

In this exercise, we're going to be taking a look at some code that's already working and figuring out how to improve it using dictionaries/sets.

The code is written in an inefficient way. We'll start by timing how long it takes with the current implementation, then doing your improvement and timing it again.

Take a look at the example code in `efficiency.py`. We'll start with the first question.

1. Run the first example using `%time` in `ipython`. Here is the code to run it:

    ```python
    from src import efficiency
    with open('data/wordlist.txt') as f:
        words = [line.lower().strip() for line in f]
    %time invalid = efficiency.invalid_words(words, 'data/frankenstein_small.txt')
    ```

    This should give you output of how long this took to run. **Write this value down.** (You can try running it on the full Frankenstein file, but you probably don't want to wait for that).

    Note: The best way to copy this into `ipython` is to copy it normally and then type `%paste` in `ipython`.

2. Make your improvements to the `invalid_words` function. You will need to run `reload(efficiency)` in `ipython` to get the updated version.

    Make sure you didn't change the functionality of the functions by running `make efficiency`.

    Time timing it again. Is it faster?
