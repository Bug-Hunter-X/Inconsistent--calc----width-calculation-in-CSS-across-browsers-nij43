# Inconsistent `calc()` width calculation in CSS across browsers

This repository demonstrates a bug related to inconsistent width calculations using the `calc()` function in CSS across different browsers.  The issue arises when calculating a percentage-based width with a fixed pixel subtraction. Some browsers calculate the percentage first, resulting in incorrect subtractions.

## Bug Report

The CSS rule `width: calc(50% - 10px);` produces varying results based on the browser. The expected behavior is for the element to have a width of 50% of its parent's width minus 10 pixels. However, inconsistencies occur, primarily due to the order of operations in the `calc()` function being handled differently.

## Solution

A workaround involves creating a container element with a defined width and applying `calc()` to this container. This ensures consistent calculation across different browsers.  Another solution might be using flexible box model or grid layout for better control over element sizes.  See the `bugSolution.css` file for example solutions.