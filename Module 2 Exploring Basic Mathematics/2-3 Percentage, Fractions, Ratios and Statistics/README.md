# Percentage, Fractions, Ratios, and Statistics

These mathematical concepts are the bread and butter of responsive design, accessibility, and data analysis in web development.

## 1. Percentages (%)

In CSS, percentages are relative. They allow layouts to adapt to different screen sizes (mobile vs. desktop).

- **Widths**: `width: 50%;` means the element takes up half of its parent's width.
- **Calculations**: If a container is 1000px and a child is 20%, the code engine calculates `1000 * 0.20 = 200px`.

## 2. Fractions

While we often use decimals (`0.5`), thinking in fractions helps with grid layouts.

- **Grid Systems**: A standard web layout often splits the screen into 12 columns. An element might span 1/3 (4 columns) or 1/2 (6 columns) of the screen.
- **Typography**: Line height is often expressed as a multiplier (fraction) of the font size.

## 3. Ratios

A ratio compares two quantities.

- **Aspect Ratio**: Critical for images and videos. Standard video is **16:9**. If you ignore this, images look stretched or squashed.
  - _CSS_: `aspect-ratio: 16 / 9;`
- **Contrast Ratio**: Essential for Accessibility (a11y). Text text must have a sufficient contrast ratio against the background (e.g., 4.5:1) to be readable by visually impaired users.

## 4. Statistics

- **Analytics**: Understanding user behavior (bounce rates, conversion rates) involves interpreting statistical data.
- **Performance**: "Average load time" vs. "95th percentile". The 95th percentile is often more important because it tells you how slow the site is for the slowest 5% of users.
