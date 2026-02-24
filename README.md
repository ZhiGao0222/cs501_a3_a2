# Assignment 3, Question 2: Profile Screen (Box Layout)

## Description
This project implements a visually polished Profile Screen using Jetpack Compose. It specifically focuses on mastering the `Box` layout to create a complex overlapping UI, mimicking a classic social media profile header. 

## Requirements Met

### 1. Box Layering & Overlap (12 Points)
- **Background**: Uses a base `Box` with a `Brush.verticalGradient` background.
- **Foreground Avatar**: Uses a `Surface` shaped as a circle layered on top of the background.
- **Overlay Card**: Implements a classic "profile card" look by placing a `Card` that partially overlaps the background header and sits perfectly beneath the avatar.
- **Intentional Positioning**: Heavily utilizes `align(Alignment.TopCenter)` and `align(Alignment.BottomCenter)` within the `Box` scope to control the placement of these layers.

### 2. Modifier Techniques (8 Points)
- **`clip(CircleShape)`**: Applied to the avatar's `Surface` to create a perfect circle.
- **`offset`**: Used `offset(y = 100.dp)` on the avatar's container to push it down across the boundary between the background and the overlay card.
- **`zIndex`**: Explicitly used `zIndex(0f)`, `zIndex(1f)`, and `zIndex(2f)` to guarantee the correct rendering order (Background -> Card -> Avatar).
- **Shadow / Elevation**: Added depth using `CardDefaults.cardElevation(defaultElevation = 6.dp)` on the overlay card.
- **Fixed Size**: Applied `size(96.dp)` to strictly constrain the avatar's dimensions.

### 3. Material 3 Components (3 Points)
Integrated over 5 Material 3 components to ensure visual polish and consistency, including:
- `Scaffold` & `TopAppBar` (Transparent container color)
- `Card` & `Surface`
- `FilledTonalButton` & `OutlinedButton`
- `AssistChip`
- `HorizontalDivider`
- `Icon` & `Text`

## Screenshots
![Profile Screen Screenshot](screenshot2.png)

## AI Disclosure (2 Points)
I used Google's Gemini AI to assist me with specific formatting, component updates, and rubric verification:
1. **Material 3 API Migration**: AI advised replacing the deprecated `Divider` component with the modern `HorizontalDivider` to adhere to the latest Material 3 guidelines and prevent compilation warnings.
2. **Rubric Verification**: AI helped cross-check my code against the assignment rubric to ensure that all required Modifiers (`zIndex`, `offset`, `clip`, `elevation`) and Box layering alignments were explicitly and correctly demonstrated.
3. **Dummy Data & Layout Polish**: AI provided suggestions on how to structure the layout inside the overlapping Card to make the user information (Name, Major, Stats) look balanced and visually appealing.
