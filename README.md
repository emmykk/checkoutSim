# checkoutSim
This was a project I completed for my Data Structures class.
The simulator can be run by executing python3 main.py in your console of choice.

Key features:

- Runs a discrete event simulator for customers in checkout lines (the specific stats of the checkoutlines are input by the user, e.g. # of lines, length of simulator, etc.)

- Assigns a customer to the shortest checkout line based on the current wait time for a given checkout line.

- Opens a new line once the average wait time for the shortest-line-by-wait-time reaches the maximum threshold. 

I chose to determine which line to source customers for the new line by using a min heap / priority queue, with the priority being determined by the negative current total wait time for that line (that is, we'll source customers for this new line from the line with the longest wait time first).

Customers are stored in a deque initially as well in order to facilitate easily removing them from checkout lines.

- Outputs statistics about customer wait times per cashier-line, and so forth.