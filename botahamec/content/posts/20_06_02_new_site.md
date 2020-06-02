---
title: "New Website! Hooray!"
date : "2020-06-02T10:13:42-04:00"
tags : ["site", "hugo", "web"]
---

Hello, everyone! Welcome to my new site. If you've seen the old one, then you know that looked remarkably terrible. Not only did it look like a dump, it was horrible to work with. Have you ever tried doing pure HTML code blocks? It's a pain. Now that issue is fixed by using ***__MARKDOWN__!*** Look at this:

```rust
fn main() {

	const MAX_NUM = 40;

	let mut a = 0;
	let mut b = 1;
	let mut c;

	for _i in 0..MAX_NUM {
		c = a + b;
		a = b;
		b = c;
		println!("{}", b);
	}
}
```

A working fibonacci sequence in Rust! With beautiful code and syntax highlighting! This will be very useful in the future.

# How it was made

The new site uses a tool called Hugo. Hugo is a static site generator created using ~~Go~~ a language which shall not be named. It can convert your markdown files into a proper HTML website. It even supports themes!

> Does this mean your making Hugo tutorials now?

Ah, it's my old friend, Captain Miscellaneous. I'm so glad you could join us. Actually, [good Hugo tutorials](https://www.youtube.com/watch?v=qtIqKaDlqXo&list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3) already exist, and there's no way I could do anything better, so no. Unless my production quality drastically improves, there will be no Hugo tutorials.

I used Github Pages for hosting. It's nice for personal sites. Btw, thanks to [Nick](https://www.thinkingmuchbetter.com) for showing me Hugo.

## Drawbacks of Hugo

The Projects page is now absolutely abhorrent. I hate it with a passion. I don't like how I need to put dates on all of my projects, and each one is just a dinky line. **I WANT BLOCKS!** I'm also too lazy to and terrible at design to make my own theme, so I'm using the Coder theme. I've thought about making my own Markdown compiler to fix this issue, but I have no idea what the theme format would look like, so I'm kinda stuck with this for now. :cry:

# Future of the Blog

I want to do some tutorials on here, and possibly some more in-depth versions of some of my videos. I wanted to explain the problems with my BOTA_BASIC language in a video, but now that I have a blog, it will be much easier to do that here. Most of my videos could probably be blogs to be honest, but I think they'll be more engaging and more lucrative on YouTube, so I'll still keep that.

# Captain Miscellaneous Time

###### When's your next Discord bot tutorial?

I don't know. I'm feeling lazy, so who knows

###### Are you ever gonna benchmark BOTA_BASIC?

Oh! Yeah. My plan was to write a couple of things in Assembly before I do that to get a fastest possible program. The problem is that I don't have a very good grasp on Assembly right now. I managed to write a Fibonacci program, and it ended up not being much faster than the version I wrote in Rust, so it's probably unnecessary

###### I would like to see that Fibonacci program

Yeah, I want to make a timelapse video of that. I have it recorded, but my Linux desktop doesn't have a webcam at the moment (it's broken) so I'm waiting for that to arrive first.

###### Why am I so indented?

Good question. I hate this indenting. Somebody please fix this.