# Tangerine (뭐머귤래) — Recipe App for One-Person Households

**Tangerine** is a **2020 team project** for people living alone, centered on finding, viewing, creating, and managing recipes. The original system combined a Java Android application with PHP endpoints and a MySQL database.

This repository is a [fork of the original team repository](https://github.com/icymunchhhiip/Tangerine). It primarily contains the **Android client**, not the original PHP backend or MySQL database setup. It is preserved as a historical team project and has not been revalidated on modern Android devices.

## Recipe workflow

- **Browse recipes:** the home screen and paginated recipe list display available recipes.
- **Search and filter:** recipe-search screens support criteria such as name, category, difficulty, tools, and cooking time.
- **View recipe details:** the detail screen displays ingredients and cooking steps.
- **Create and edit recipes:** the recipe editor implements entry and modification flows.
- **Save and revisit recipes:** account-linked saved/written recipe screens are represented in the client.

Additional team-developed modules cover refrigerator ingredients, a community marketplace and cooking tips, profile management, and location-aware features. These modules are part of the overall team application; they are not listed as my individual contributions.

## My contributions

My work on the original team project focused on:

1. **Database:** built the recipe and ingredient-related database.
2. **Android UI and functionality:** developed recipe viewing, registration, editing, and listing.
3. **Backend communication:** implemented PHP-based data exchange for recipe functions.

The Android source includes related classes and PHP-facing Retrofit routes. The PHP source and database schema are not included here, so the full backend behavior cannot be independently reproduced.

Git history includes commits from multiple teammates, and the repository was maintained/uploaded through the original team account. There is also a commit under the author name **노강은 (Kangeun Noh)**, but commit ownership alone does not describe the complete division of work; the responsibilities above come from the original project description.

## Technology

- **Android:** Java, Android SDK 29, AndroidX, fragments, navigation and RecyclerView
- **Networking:** PHP-based API, Retrofit, Gson, OkHttp, Volley
- **Database:** MySQL (original server-side component, not included here)
- **Other team modules:** Kakao login, map/location functionality, image loading and upload

## Code map

```text
app/src/main/java/com/sixsense/tangerine/
  home/
    RecipeListFragment.java       Recipe listing
    InRecipeActivity.java         Recipe details
    SearchFragment.java           Recipe search
    write/WriteRecipeActivity.java Recipe creation and editing
  network/
    HttpClient.java               Retrofit client configuration
    HttpInterface.java            PHP API route definitions
    InRecipe.java                 Recipe response models
    SelectedRecipe.java           Recipe request data
  ref/                            Refrigerator/ingredient screens
  community/                      Cooking tips and marketplace
  login/                          Authentication integration
  setting/                        Profile and saved-content screens
```

## Reproduction and limitations

This is **not a turnkey build**. The repository includes older Android dependencies and references external services and legacy backend addresses. The PHP source, MySQL schema, service configuration, and original data set are missing.

A future restoration would require migrating the Android toolchain, providing a compatible backend and database, replacing hard-coded endpoints with configurable HTTPS services, reviewing identity and map integrations, and running device/integration tests.

**Security note:** Existing client code uses fixed HTTP addresses and body-level network logging. These are historical implementation decisions, not appropriate defaults for production authentication or personal data. The app has not undergone a contemporary security review.

No current deployment, successful modern build, automated end-to-end tests, or measured usage/performance is claimed.

## Attribution

Originally developed as a team project in 2020. This fork retains the original Git history and credits the [upstream team repository](https://github.com/icymunchhhiip/Tangerine). My responsibilities are described specifically above; no sole authorship of the complete app is implied.
