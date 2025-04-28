### Name:
Rosie Baish

### Department:
Computer Science

### Contact:
rvb30

### Project details:
John C. Reynolds wrote [the canonical paper on Separation Logic](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1029817)

In it he lays out the following model of a program.
The `store` is a total function from variable names to values.
The `heap` is a partial function from values to values, which is defined over the values that the program has access to.
(A partial function is one which is only defined on some elements of the domain, so the function is from integers to integers, but is only defined on the even integers. A total function is one that is defined on all elements of the domain)

He defines a separation logic as a set of assertions which are of the form `store -> heap -> {true, false}`
For example, the assertion `true` is the function `f(s, h) -> true`

This definition works, but any proofs require working with partial functions for the heap which are inconvenient.

I came up with an alternative formulation where the heap is a total function from values to values, and assertions evaluate to a pair `(b, m)` where `b` is `{true, false}` and `m` is a set of addresses on the heap which it claims ownership for.

My hypothesis is that these definitions are equivalent, and that for an assertion `q`, a heap `h` and a store `s`, the the assertion evaluates to true under Reynold's definition if and only if `b \and (q tight \implies h = m)`
`q` being tight is a measure of whether `h` is the smallest heap that `q` is true in, although there is a more formal definition.

I have proved this true for basic logic and for the separating conjunction, but have not proved it true for the separating implication. (explanation of that that is are in the paper)
The project is to figure out what exactly it would mean for a separating implication to be tight, and then add an extra case to each of the lemmas in the proof.

Once the proof were complete there may be scope to write it up as a paper. I am not certain whether it is 'paper-worthy' or not, so part of the project would be figuring that out as well.

The proof thus far can be found [here](https://github.com/RosieBaish/lean-sep-logic)