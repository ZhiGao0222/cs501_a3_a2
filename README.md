# Assignment 3, Question 2: Profile Screen (Box Layout)

## Description
This project implements a visually polished Profile Screen using Jetpack Compose. It specifically focuses on mastering the `Box` layout to create a complex overlapping UI, mimicking a classic social media profile header. 

## Key Features

* **Advanced Box Layering**: Implements a multi-layered UI using `Box` to stack a gradient background, an overlapping profile card, and a centered avatar.
* **Intentional Positioning**: Heavily utilizes `align(Alignment.TopCenter)` and `align(Alignment.BottomCenter)` combined with `offset(y = 100.dp)` to achieve a classic "floating avatar" effect.
* **Depth & Elevation Control**: Explicitly manages the rendering order using `zIndex` and adds visual depth through `CardDefaults.cardElevation` on the profile container.
* **Material 3 Visual Polish**: Integration of over 5 M3 components including `Scaffold`, `CenterAlignedTopAppBar`, `FilledTonalButton`, `AssistChip`, and `HorizontalDivider` for a consistent design language.
* **Modifier Precision**: Employs specific modifiers such as `clip(CircleShape)` for circular avatars and `size(96.dp)` for strict constraint management.
  
## Screenshots
![Profile Screen Screenshot](screenshot2.png)

## AI Disclosure (2 Points)
I used Google's Gemini AI to assist me with specific formatting, component updates, and rubric verification:
1. **Material 3 API Migration**: AI advised replacing the deprecated `Divider` component with the modern `HorizontalDivider` to adhere to the latest Material 3 guidelines and prevent compilation warnings.
2. **Rubric Verification**: AI helped cross-check my code against the assignment rubric to ensure that all required Modifiers (`zIndex`, `offset`, `clip`, `elevation`) and Box layering alignments were explicitly and correctly demonstrated.
3. **Dummy Data & Layout Polish**: AI provided suggestions on how to structure the layout inside the overlapping Card to make the user information (Name, Major, Stats) look balanced and visually appealing.
