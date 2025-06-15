---
layout: single
title: Benchmarking a new analysis in Python
toc: true
toc_label: Python benchmarking
toc_icon: "fa-solid fa-terminal"
author_profile: true
---

White matter pathways are like the information highways of the brain, connecting different bits of grey matter and allowing information to travel between regions. Around 50% of the human brain's total mass is white matter, and one of the major evolutionary innovations of our primate ancestors was the expansion of [the white matter pathways to the prefrontal cortex](https://www.google.com/books/edition/The_Evolution_of_Memory_Systems/rcpLDQAAQBAJ). When white matter goes wrong, it can lead to devastating conditions like multiple sclerosis.  

{% include figure popup=true image_path="/assets/images/GraysAnatomy_1918.png" alt="medical illustrations depicting axial and coronal sections of the right brain hemisphere" caption="*White matter runs along the interior of the brain, connecting different regions of cortical grey matter. Illustrations from Gray's Anatomy, 1918 edition.*" %}

So, white matter is important for a variety of reasons.  

The trouble is, it can be difficult to study. For brains we know a good deal about – say, the brains of adult humans – we have some pretty great tools. So-called white matter atlases are an *excellent* resource for identifying white matter connections in well-studied brains, and new atlases are being developed every year. But what about the brains we *don't* know as much about? For anyone wanting to study white matter in an unusual brain, things get a lot trickier.  

In [my first post](https://jasperehunt.github.io/brain-sorting), I described how I developed a data-driven technique for comparing white matter across non-human species. This technique addresses an important gap for researchers, but in order to be useful, it also has to *perform well*.  

Once I had built the tool, the next step was to do some benchmarking. Just what are this tool's limitations, and where does it excel?  

## What does success look like?  

### The gold standard: atlas-based tractography  

A white matter atlas is like a recipe book, containing all the information needed to reconstruct the white matter tracts of the brain. This includes information about where a tract begins and ends, which regions it passes through, and which regions it *does not* pass through. This is the current gold standard in tractography, tractography being the technique of reconstructing white matter tracts from imaging data.

The trouble is, it's incredibly time- and labour-intensive to develop new white matter atlases. Nevertheless, any new technique should be compared against atlas-based tract reconstruction, to get a sense of its overall performance.  

### Reliability and validity 

A useful instrument must offer accurate, consistent, and interpretable data. The way we assess some of these desirable qualities is by determining the tool's *reliability* and its *validity*.  

{% include figure popup=true image_path="/assets/images/reliability_and_validity.png" alt="marks are arranged on a series of dartboards, demonstrating examples of good vs. poor reliability and validity" caption="*A dartboard metaphor is frequently used to illustrate the differences between reliability and validity.*" %}

What are we aiming for? Imagine four dartboards. The shots on the first target are reliable, as they hit the same point repeatedly; however, the shots all missed the bulls-eye in the centre. This target is reliable, yet invalid. The second target shows validity, as the shots were centred around the bulls-eye; however, the shots are unreliable, spread across the entire breadth of the target. The third target is neither valid nor reliable, as the shots are spread widely across the upper portion of the target. Finally, the fourth target represents both reliability and validity; the shots consistently hit the bulls-eye target's centre.

A *reliable* instrument is one which will give you the same result repeatedly, while a *valid* instrument is one which measures what it's supposed to measure. This is a useful framework to keep in mind as we assess our new tractography approach. Is the technique doing what we want it to, and is it doing so consistently? Ideally, a new tool will be both reliable and valid.  

## Benchmarking in Python  

## Usability  

## Key takeaways  

{% include figure popup=true image_path="/assets/images/dartboard_banner.png" alt="a well-used dartboard hanging on a wall" caption="*Just like in darts, the name of the game is to hit the mark early and often.*" %}