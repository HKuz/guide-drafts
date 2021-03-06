# Wrap Radio Buttons in a Fieldset Element for Better Accessibility

## Challenge Description

Our next form topic will cover accessibility of radio buttons. Each choice is given a `label` with a `for` attribute tying to the `id` of the corresponding item as we covered in the last challenge. Since radio buttons often come in a group where the user must choose one, there's a way to semantically show the choices are part of a set. The `fieldset` tag surrounds the entire grouping of radio buttons to achieve this. It often uses a `legend` tag to provide a description for the grouping, which is read by screen readers for each choice in the `fieldset` element.

The `fieldset` wrapper and `legend` tag are not necessary when the choices are self-explanatory, like a gender selection. Using a `label` with the `for` attribute for each radio button is sufficient.

Here's an example:

```html
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="ground">Choice Three</label>
  </fieldset>
</form>
```

## Instructions

CamperCat wants information about the ninja level of his users when they sign up for his email list. He's added a set of radio buttons, and learned from our last lesson to use `label` tags with `for` attributes for each choice. Go CamperCat! However, his code still needs some help. Change the `div` tag surrounding the radio buttons to a `fieldset` tag, and change the `p` tag inside it to a `legend`.

## Challenge Seed

```html
<body>
  <header>
    <h1>Deep Thoughts with Master CamperCat</h1>
  </header>
  <section>
    <form>
      <p>Sign up to receive CamperCat's blog posts by email here!</p>
      <label for="email">Email:</label>
      <input type="text" id="email" name="email">
      <!-- Only make changes below this line -->
      <div>
        <p>What level ninja are you?</p>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Developing Student</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">Master</label>
      </div>
      <!-- Only make changes above this line -->
      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-yummy trifecta that is lasagna...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightening speed. But chin up, fellow fighters, our time for victory may soon be near...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
  <footer>&copy; 2016 CamperCat</footer>
</body>
```

## Challenge Tests

```
assert($('fieldset').length == 1, 'message: Make sure to use a <code>fieldset</code> tag instead of a <code>div</code> around the radio button set.');

assert($('legend').length == 1, 'message: Make sure to use a <code>legend</code> tag instead of the <code>p</code> tag around the text asking what level ninja a user is.');

assert($('div').length == 0, 'message: Change the <code>div</code> tag to a <code>fieldset</code> tag.');

assert($('p').length == 4, 'message: Change the <code>p</code> tag to a <code>legend</code> tag.');
```

## Challenge Solution

```html
<body>
  <header>
    <h1>Deep Thoughts with Master CamperCat</h1>
  </header>
  <section>
    <form>
      <p>Sign up to receive CamperCat's blog posts by email here!</p>
      <label for="email">Email:</label>
      <input type="text" id="email" name="email">
      <!-- Only make changes below this line -->
      <fieldset>
        <legend>What level ninja are you?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Developing Student</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">Master</label>
      </fieldset>
      <!-- Only make changes above this line -->
      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-yummy trifecta that is lasagna...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightening speed. But chin up, fellow fighters, our time for victory may soon be near...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
  <footer>&copy; 2016 CamperCat</footer>
</body>
```
