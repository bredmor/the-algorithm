# The Algorithm
![The Algorithm](/img/logo.png?raw=true)

The perfect algorithm for sorting posts on social media timelines. A powerful sort that almost magically shows every user what they want to see based on their interests. Free to use and adapt to your favorite datastore!

## Concept
Every social media network has a different algorithm to show its users content to eachother. From Twitter and Facebook to Tiktok and Tumblr, there's a highly polished, data driven set of rules to make sure each user sees the right posts. This project creates a sort of "grand unified algorithm" that demonstrably and uncorruptably adapts these algorithms to the absolute pinnacle of content selection.

## The Algorithm Itself

### Prerequisite
> #### Case α
Suppose each **User** `u` follows `n` other **Users** `f`.

All `f|u` own `>=0` **Posts** `p`.

Each `p` has a **Timestamp** `z`.

The **Timeline** `t` is the result of all `p` owned by `f`.

![Case Alpha](/img/case_alpha.png?raw=true)

> #### Case β
Suppose each **User** `u` owns `>=0` **Posts** `p`.

Each `p` has a **Timestamp** `z`.

The **Timeline** `t` is the result of all `p` in the system.

![Case Beta](/img/case_beta.png?raw=true)
-----

### Selection
**In Reverse Precedence**:

1. Limit the selection of `p` from `t` to **Total number of `p` to show per loading call** `x`.
2. As `a`, for the current time `c`, order `p` by `z` in descending order.
3. Return `a` as the call result.

![Selection](/img/selection.png?raw=true)

-----

### Rendering
Display each `p` in returned order from `a` to the End User, ordered from top of the viewport to bottom.

-----

## Caveats
- End Users may not initially understand this selection of Posts. Most social media users expect a semi-random display of Posts and having a predictable selection of content from Users they expect, in the order they were posted may confuse them.
- End Users may see Posts from Users they assumed died or left your site entirely.
- You may see a stark decrease in engagement with your Support team, specifically a lack of messages complaining about not seeing friends posts. Not to worry, this is normal.
