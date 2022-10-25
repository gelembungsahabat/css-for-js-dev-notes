# Responsive and Behavioural CSS

## Mobile-first vs desktop-first
There are two distinct ways we can write the media query:
```
.signup-button {
  color: deeppink;
  font-size: 1rem;
}

@media (max-width: 400px) {
  .signup-button {
    font-size: 2rem;
  }
}
```
```
.signup-button {
  color: deeppink;
  font-size: 2rem;
}

@media (min-width: 401px) {
  .signup-button {
    font-size: 1rem;
  }
}
```
The first snippet is known as desktop-first, since our default styles (the ones not inside @media) target desktop devices, and then we specify overrides for mobile devices. By contrast, the second snippet is mobile-first, since the main styles are for mobile devices (400px or smaller).

To be clear, the end result is the same. These are two different roads to the same place. But the mental model is different.

<br>
<br>

### Which should I use?
When starting a new project, you'll need to pick whether you take a desktop-first or a mobile-first approach.

Honestly, I don't believe that there is a single "right" answer to this question. This is one of those unsatisfying "it depends" situations.
<br>
<br>

### Here's how I think about it:

If the project will be viewed primarily by folks on mobile devices, it makes sense to go mobile-first. This is becoming more and more common, as mobile usage eclipses desktop usage, but it depends on the site. When I worked at Khan Academy, we had very little mobile traffic, because it was heavily used inside school computer labs and on school-assigned Chromebooks, and because we had a mobile app for mobile users.

Another factor to consider: are you designing the project, in addition to implementing it? If so, it can be helpful to think in mobile-first terms, because it's easier to add than to take away. If you start from a desktop perspective, you'll need to find a way to shrink everything for mobile, which can be really tricky. Better to start from mobile, and work your way up.

Ultimately, though, the most important thing is to be consistent with the approach. If you decide to build mobile-first, you should almost always use min-width media queries. It can be very confusing if you mix min-width and max-width media queries.