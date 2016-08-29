# android-anim-viewpager-transitions
Sample example for transitions between fragments within viewpager
This sample project shows how to do screen slides within a ViewPager.

## Project details
* Creates a ScrollView with TexView within it
* Creates a fragment
* Adds a ViewPager within in Main Activity's layout
* Customizes the slide animation with PageTransformer
	* Zoom-out page transformer

## Zoom out custom animation
To provide custom animation to screen slide following steps are followed:

1. Implement the ViewPager.PageTransformer interface and supply it to the view pager. 
2. transformPage() method is implemented to simulate Zoom-out page feel.
3. Based on the position of the pages on the screen, you can create custom slide animations by setting page properties with methods such as setAlpha(), setTranslationX(), or setScaleY().
4. The position parameter indicates where a given page is located relative to the center of the screen. It is a dynamic property that changes as the user scrolls through the pages. When a page fills the screen, its position value is 0. When a page is drawn just off the right side of the screen, its position value is 1. If the user scrolls halfway between pages one and two, page one has a position of -0.5 and page two has a position of 0.5. 
5. This custom Pagetransformer is passed to setPageTransformer() on ViewPager

![Alt text](viewpager-slides.gif?raw=true "Video Walkthrough")

## Open-source libraries/code references
https://developer.android.com/training/animation/screen-slide.html

# Attribution
This code was created by Shrikant Pandhare in 2016 for use in CodePath sessions.
