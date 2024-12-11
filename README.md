# Tailwind CSS Uncommon Class Error

This repository demonstrates a common yet often overlooked error in Tailwind CSS: using a class that hasn't been included in your `tailwind.config.js` file's `content` array.

## The Problem

If Tailwind doesn't find a class within the specified files (or glob patterns) in `content`, it won't generate the corresponding CSS. This leads to the class being unrecognized, resulting in the default browser styling being applied, or in some cases no styling at all.

## Solution

Ensure your `tailwind.config.js` file's `content` array correctly includes all files where you're using Tailwind classes. This often involves updating the array to include newly added components or templates.  Using a glob pattern such as `'./src/**/*.{js,jsx,ts,tsx}'` is often helpful.