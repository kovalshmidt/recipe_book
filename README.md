# Recipe Book Collaboration Instructions

Welcome to the Recipe Book project! Follow the steps below to contribute your unique recipes to the repository.

---

## 1. Clone the Repository

To start, clone the repository to your local machine by running:

```
git clone https://github.com/kovalshmidt/recipe_book.git
```

Move to the repository:

```
cd recipe_book
```

Explore the `Recipe_Book.md` file.

The repository has two branches: `master` and `development`.
You should work with the `development` branch.


## 2. Create Your Branch and Add Recipes

Your task is to add three unique recipes to each section (Breakfasts, Main Dishes, Soups, Salads, Desserts, Cocktails).
Before making any changes, create a new branch from development. Name your branch using this format:

`<initials>_<day_of_birth>_<recipe_section>`

example: 
```
git checkout -b vk_27_main_dishes
```

Open the `recipe_book.md` file and add your recipes to the appropriate section. Use the following format for each recipe:

---

### Recipe Name
- **Ingredients**: List the ingredients here.
- **Instructions**: Provide clear instructions on how to make the dish.
<div style="text-align: right;">
    <small>author_name</small>
</div>

---

Example:
```
---

### Spaghetti Bolognese
- **Ingredients**: Spaghetti, minced meat, tomatoes, onions, garlic, olive oil.
- **Instructions**: Boil the spaghetti. In a pan, cook the minced meat with onions and garlic, add tomatoes, and let it simmer. Mix with the boiled spaghetti.
<div style="text-align: right;">
    <small>Vitaliy</small>
</div>

---
```
Between the recipes there should be only one line defined by "---".

Make sure your recipe hasn’t already been added. Frequently check for updates by pulling the latest changes from the development branch:
```
git checkout development
git pull origin development
```

You can also use `git diff` to compare your changes with those on origin before committing.

## 3. Commit Your Changes

Once you have added a recipe, commit your changes with a message indicating what you added or updated:
```
git add recipe_book.md
git commit -m "added Spaghetti Bolognese"
```
## 4. Merge Changes
After you have created three recipes in your branch, merge the latest changes from the development branch into your custom branch to ensure your branch is up to date:

```
git checkout development
git pull origin development  # Update local development with any changes
git checkout vk_27_main_dishes   # Switch back to your branch
git merge development         # Merge changes from development into your branch
```
Resolve any conflicts you may encounter.

## 5. Tag Your Merge Commits
After merging your branch into `development`, tag your merge commit with a descriptive tag name. Use one of the following formats:

```
git tag -a <intials>_<section_in_lowercase> -m "Description"
git tag -a vk_main_dishes -m "Merged vk_27_main_dishes into development"
```
Push your tags to origin.

## 6. Push Your Changes
Once the merge is successful and there are no conflicts, push your branch back to the development branch:
```
git checkout development
git merge vk_27_main_dishes      # Merge your changes into development
git push origin development   # Push changes to the remote repository
```
If you encounter any merge conflicts, carefully resolve them and ensure that your final recipe is added correctly.


## Optional
Create a branch for each section `<vg>_<initials>_<year_of_birth>_<recipe_section>` in which you have to modify each recipe that was introduced by you, so that it becomes vegetarian.
Replace meat and fish with tofu, seitan, soy meat or any vegetarian alternative.

```
git commit -am "vegetarian Spaghetti Bolognese"
```

This time `rebase` your changes into `development`.
Resolve any possible conflicts before pushing to origin.
