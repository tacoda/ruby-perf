# Ruby Performance

- Memory consumption and garbage collection are among the major reasons why Ruby is slow.
- Ruby has a significant memory overhead.
- GC in Ruby 2.1 and later is up to five times faster than in earlier versions.
- The raw performance of all modern Ruby interpreters is about the same.
- The 80-20 rule of Ruby performance optimization: 80% of performance improvements come from memory optimization, so optimize memory first.
- A memory-optimized program has the same performance in any modern Ruby versions.
- Ruby 2.1 is not a silver performance bullet; it just minimizes losses.

1. Is Ruby the right tool to solve my problem?

Ruby is a general-purpose programming language, but that doesn’t mean you should use it to solve all your problems. There are things that Ruby is not so good at. The prime example is large dataset processing. That needs memory: exactly the sort of thing that you want to avoid.

This task is better done in a database or in background processes written in other programming languages. Twitter, for example, once had a Ruby on Rails front end backed by Scala workers. Another example is statistical computations, which are better done with, say, the R language.

2. How much memory will my code use?

The less memory your code uses, the less work Ruby GC has to do. You already know some tricks to reduce memory consumption—the ones that we used in our example: line-by-line data processing and avoiding inter- mediate objects. I’ll show you more in subsequent chapters.

3. What is the raw performance of this code?

Once you’re sure the memory is used optimally, take a look at the algo- rithmic complexity of the code itself.
