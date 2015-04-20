# forestfire-rs

A simulation of a forest fire. It starts with a 30x30 forest, lights the center
tree on fire, and then burns until all burning trees have burned out.

On each iteration, each un-burned tree has a 10% chance to catch fire from a
neighboring burning tree and each burning tree has a 30% chance to burn out.

Currently, the software is setup as a double-buffered mechanism. It's my
intention to use this to introduce parallelism in the future.

A screen-capture of a single [run is available](https://youtu.be/Trrow1D23nw).

# Example

Green trees are marked with a `^`. Burning trees are marked with a `#`. Burned
trees are marked with a `_`.

Here's the forest when it's first set on fire.

```
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^#^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
```

Here's the forest part way through the burn.


```
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^_^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^#__^^^^^^^^
^^^^^^^^^^^^^^^^^#^^#_^#_^^^^^
^^^^^^^^^^^^^^^^^^______^^^^^^
^^^^^^^^^^^^^^^^^^^_^__^^^^^^^
^^^^^^^^^^^^^^^^^^^____^#^^^^^
^^^^^^^^^^^^^^^^^^____^^^^^^^^
^^^^^^^^^^^^^^^^^^__^^^^^^^^^^
^^^^^^^^^^^^^^^_^_^_^^^^^^^^^^
^^^^^^^^^^^^^_^^____^^^^^^^^^^
^^^^^^^^^^^^^_______^^^^^^^^^#
^^^^^^^^^^^^^________^^^^^^#^#
^^^^^^^^^^^__^_^_____^^__^__^^
^^^^^^^^^^^________^^_^_____#^
^^^^^^^^^^^____________^______
^#^#^^^^^^_________________^_^
^#^__^_^__________________#___
^^^__^^___^_^____#__________^_
^^^^#_#___^^^________#_^___^_^
^^^^_^_^__^^^^_______##^#^_^##
^^^^##_^^^^^^^^_^___^#^^_^^^#^
^^^^^___^^^^^^^^____^##_#^_#^^
^^^^^^#^_^^^^^^^_____#_^^^^^^^
^^^^^^#^^^^^^^________^^_^^^^^
^^^^^^^^^^^^^________^^^^^^^^^
^^^^^^^^^^^^^^______#^#^^^^^^^
^^^^^^^^^^^^^#_^_^__^^#^^^^^^^
^^^^^^^^^^^^^^^^#__^#^^^^^^^^^
```

Here's the forest when there are no more burning trees.

```
^________^^^__^_^_^__^^_____^_
_________^________^__________^
______________^____________^^^
________^_________^_______^_^_
___^____________^_____^__^^__^
^_______^^____________________
_________^_____________^^^____
_____^______^_________________
^__^________^____^____________
____^_______________^________^
^^__^^_______^^_^_^_________^_
_______^______^^____^___^^____
^__________________________^__
________^___________________^_
_____________^_^_____^^_____^_
___________________^^_^______^
_____^_^_^^___________________
^_^_^____^_________________^_^
^_____________________________
__________^_^_______________^_
__________^_^______________^_^
^____^_^_____^________________
_______^______^_^_____^_______
_______________^______________
____________^___________^__^_^
___^_^_____________________^^^
____^^_________________^^__^^^
___^_^_______^___________^^^^^
_^_^_____^_____^_^__^__^^^^^^^
^^^^____^____^_^___^_____^^^^^
```
