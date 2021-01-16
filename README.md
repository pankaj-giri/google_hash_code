# This is the solution to the Google Hashcode 2020 Qualifier

## Problem Statement overview

This involves reading information about several libraries from a file, which has a list of books, and the information about scores for each book. Each library has a certain signup time associated. The problem is about Optimizing between signup time and scanning the books so that the scores can be maximized.

More about the problem statement and the data can be accessed from the following.

* https://storage.googleapis.com/coding-competitions.appspot.com/HC/2020/hashcode_2020_online_qualification_round.pdf
* https://storage.googleapis.com/coding-competitions.appspot.com/HC/2020/qualification_round_2020.in.zip

## Algorithm Approach:

### Approach 1

1. Sort the libraries by the signup times in the ascending order
2. Check if the number of days remaining is greater than the scan days...

    ```scan_days = no_of_books_in_lib/can_ship```

   if scan_days > number of remaining days, then add all the books from the library for scanning,
   else include the books in the order of their scores, with the higher scores first.

With this approach, we have the following scores for each of the sample input files..

1. a_example = 21
2. b_read_on = 5822900
3. c_incunabula = 5467966
4. d_tough_choices = 4109170
5. e_so_many_books = 3644730
6. f_libraries_of_the_world = 2420875

### Approach 2

Uses a heuristic that the score should be high, with a lower number of books and the number that can ship per day should be high.

```score*can_ship/number_of_books``` should be as high as possible.

==================================================================================




