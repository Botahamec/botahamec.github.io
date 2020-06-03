---
title: "Ideas for Projects to Do"
date : "2020-06-03T10:13:42-04:00"
tags : ["ideas"]
categories: ["technology"]
---

I have a lot of ideas for future projects. I'll probably never get to do most of them. So let me list some of them so that you may give them a try.

## Sudoku Solver

Yes, I know many [people have done this already](https://www.youtube.com/watch?v=G_UYXzGuqvM). I really like the idea though so I wanna try it without looking at other people's solutions. Of course, you're free to do it in whatever way you like, but you'll probably need a GUI for it. OrbTK looks like the most promising framework to do this in if you're using Rust (but I have no experience whatsoever).

These are some suggestions for how you might go about it. I suggest skipping this part if you don't want anything spoiled. You might be able to use backtracking to do this, but that would be very inefficient. I think each square should store the possible values, which should be pretty easy to determine. If a square only has one possible value, then that becomes the new value. I think once a square has been determined, it should alert all of the other squares in the same row, column, and box to see if any possibilities can be eliminated.

## Snake AI

[Code Bullet already tried to do this](https://www.youtube.com/watch?v=tjQIO1rqTBE), but it didn't work very well. Your implementation should do it perfectly. By the way, their AI is cheating. The snake waits for the AI to make a decision before it can move. In the real world, the snake should move whether you want it to or not. You will need some multithreading to accomplish this.

Code Bullet was on the right track when he used the Hamiltonian cycle. The problem is that he skips spots at certain places to make it go faster, but actually cuts off parts of the board. The actual way to make it work faster is to generate a new Hamiltonian cycle every time the snake reaches the apple. The Hamiltoian cycle should be created in such a way that it reaches the apple as quickly as possible. There is a problem here though. The hamiltonian cycle actually requires a backtracking algorithm, which is very computationally expensive. Your task will be to optimize that.

## Tetris AI

I like Tetris. I want an AI that plays Tetris as well as possible.

I legitimately have no idea how to do this. The best idea I have is to make moves so that all of the known future pieces will be able to make a perfect fit, and then regardless of whatever piece is next, that should work too. There's almost certainly situations where this would be impossible though. :pensive:

## A BASIC

[I kinda did this](https://www.youtube.com/watch?v=28VdsLV6Lts&t=2399s), but it sucked terribly. I think I accidentally made it dynamically typed, which is why it was so hard. Don't try to do that this time

## Optimized Brainf**k

BF is a very easy language to write a compiler for. But as far as I know, nobody has tried to make a good compiler. The goal is to make a  heavily-optimized BF AOT compiler. A "good" time would probably be calculating the first 40 fibonacci numbers in less than 100 milliseconds. Although, I would be *really* impressed if it could be done in less than two milliseconds.

You are allowed to compile it to C code, and then compile the C code. As long as it creates an assembled binary. There are some instances where parts of the stack can be turned into raw variables, but sometimes you will actually need the stack. Some of the loops can probably be optimized.

## Optimized Functional Programming

The dissappointing thing about functional programming is that there are very many opportunities for optimization, but very few languages actually attempt this. Too many functional languages are interpreted. This must be fixed.

The great thing about functional programming is that it's abstract. Variables don't actually exist, so the compiler can choose what to put into memory and what not to. It can also tell pretty easily when code is being reused. Consider the following Haskell code:

```haskell
sum :: Integer -> Integer -> Integer
sum a b = a + b

sum 5 4
```

Now, how should we translate this to C code? Most people would translate it like this:

```c
int sum(int a, int b) {
	return a + b;
}

void main() {
	sum(5, 4);
}
```

But honestly, the compiler should treat it like this:

```c
#define SUM(a, b) a + b

void main() {
	SUM(5, 4);
}
```

There's an optimization opportunity when you see a function called multiple times. The same can be applied to variables. The compiler has to figure out how long to keep each variable in memory.

There's a lot more you can do. We might reach a point where there's actually a performance benefit to using functional programming instead of C.

## Making an Assembler

Yeah, this is hard. I won't do this anytime soon

## Make a Calculator

I'm thinking something like the [Numworks calculator](https://www.numworks.com/). It should be a programmable graphing calculator.

I recommend using a Raspberry Pi Zero for this project. The main reason I haven't started it is because I can't quite figure out how to make the keyboard. I have a friend who loves making her own keyboards, but somehow I don't think a mechanical keyboard is a great fit for this project. You also need an operating system. You have two options. Either write it yourself, or use Linux, and have a program run inside it. If you're going with the former, [here are some tutorials for writing an OS in Rust](https://os.phil-opp.com/). As for the latter, you may find [Core Linux](http://www.tinycorelinux.net/) useful.

## Betting Discord Bot

Make a Discord Bot with its own economy that allows users to make bets. The specific kind of bet is up to you, but my favorite idea is having users bet on which option gets the least number of bets.

I know I established myself as a Rust geek, so here are my tutorials for writing a [Discord bot in Rust](https://www.youtube.com/watch?v=sOA6rSRCqPw&list=PLPwSz_Jcam3xVjrTAYgIHvf1Jq94yrRXp). You'll also need to store data, which I plan to teach in a future tutorial. In the mean time, you'll definitely want to have [serde](https://serde.rs/).

## Github Tracker Bot

I know it's possible to use Webhooks. But how cool would it be to have a bot that's already able to do it with just a simple command? I think this is very necessary. The same applies for YouTube videos.

## Web Compiler

It takes a website, and compiles it to machine code. No more Electron!

---

So those are my ideas. I quickly wrote this up because I have another article I want to write, and I didn't want my second article ever to be a political/philosophical article. I'm too tired to listen to Captain Miscellaneous today. Goodbye.