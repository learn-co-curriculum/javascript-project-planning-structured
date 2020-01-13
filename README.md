# JavaScript Project Planning Resources

## Introduction

This is exciting stuff. Your Javascript project is an excellent chance for you to
show off everything you’ve learned about Rails by applying that knowledge to
build out your API AND apply what you've learned about JavaScript by creating
your first Single Page Application (SPA).

One of the most important processes in building any application is planning —
let's take some time to map out our project to save ourselves time and
heart/headache later. Unlike labs, projects do not have the guardrails of a
README and tests to structure your work. Instead, you need to design and plan
your features yourself. These tips should help you plan your project
effectively.

**Use this document to help you complete [this planning form][planning form]**

Tips on all aspects of the project are included here, so make sure to have a
look through!

## How to Get Started On a Successful Project Build

1. Read through the project requirements [here][project requirements] carefully
   before getting started.

2. Come up with a project idea of your own, and devote some time to a planning
   session. Think about the following:

      a. Brainstorm the problem that you want your application to solve. It's
      okay to take inspiration for the features you want to build from other
      sites or projects you've seen (it's not okay to use their code, though).

      b. Plan what features your app will have. You can write User Stories to
      help make it clear what you are planning to build.

      c. Model your domain. You need to know what the nouns in your project are
      - the objects in the 'world' of your application. It can be helpful to
      draw the relationships between your models.

      d. Plan how your features will work. [Use this form][planning form] to jot
      down your plans and submit them to us so we can see what you are planning!
      Check out the sections below on User Story and Flow Diagrams for help in
      filling out the form.

3. Create a skeleton app and push to a remote repository on Github.

4. Plan your schedule. Note that it takes most full time (40+ hrs/week) students
   between 3-7 days to complete, and can take up to 5 business days to schedule
   your project review after that.

5. Join the Slack channel #rails-js-section to connect with others who are
   working on their projects as well. Students often set up a peer review in
   advance of their project review as a way to practice talking through your
   code.

We are here to help!  Each week, there are Open Office Hour [study groups][]
specifically designed to help with your JavaScript project questions. Also, keep
an eye out for topic-based JS study groups if you feel shaky on any specific
concepts.

### Making a User Story

- Who is your User?
- What are their pain points?
- How do they use our solution to overcome this problem?

User Stories are a powerful tool for succinctly describing a set of
functionality in terms of what it allows the user to do.

Some examples of user stories:

- A user is able to view travel locations, add new travel locations, edit travel
  locations and delete travel locations.
- A user is able to review a travel location
- A user is able to edit and delete a review for a travel location

When you have written the user stories for your application, you can turn them
into the technical requirements needed to turn those stories into
working features.

### Choosing your Classes

As you turn your user stories into more clear technical specifications for
features, you can start by modeling the data that your application will store
and show. Identify the nouns in your stories, their properties, and their
relationships.

A description of the domain for the above stories might be:

- A travel location has a name, a description, a location, and an image URL
- A review has a comment and a rating
- A review belongs to one travel location (a travel location has many reviews)
- A travel location has an average rating that is calculated by its aggregate
  review ratings

Later on, you will be ready to create the database schema and application models
corresponding to this domain.

## Making an App Flow Diagram

- How is data passed around your app?
- What classes are used? What are their responsibilities?
- How can I avoid unnecessary duplication of actions?

We recommend using [draw.io][] to put together a flow diagram. It doesn’t need
to be over-complicated  - just a visual idea of your app’s structure.

You don’t have to use software for this - a photo of a (legible) hand-drawn
sketch on a napkin also works!

The following GIF shows how to make a shareable link on draw.io:

![make shareable draw.io gif](https://curriculum-content.s3.amazonaws.com/project-planning/shareable%20link.gif)

**Please make sure the image or file you share with us is accessible.**

### MVP ASAP
(Minimum Viable Product, As Soon As Possible)

Building things is hard. It's tough to predict what will be difficult in a
project. Sometimes things that appear on the surface to be easy will end up
taking hours of debugging.

With that in mind, it's important to build a Minimum Viable Product (MVP) as
quickly as possible. Instead of getting stuck on advanced features, start with a
basic working version of the application, then steadily add features piece by
piece.

### Build vertically, not horizontally

It's easy to end up having to do lots of rework and fixing depending on how you
order the things you build in your application, particularly if you build
'horizontally.'

You can visualize all the parts you of an app you need to build as a grid, with
the features along the x-axis (columns) and the different layers of the stack
along the y-axis.

A strong temptation is to build your project row-by-row. It feels easy to start by
writing all the migrations for all your models, then all the models, etc...

**Do not do this!**

If you try to build all your migrations, then all your models, then all your
controllers, then all your fetch calls, then all your view logic, you will have
a bad time. Inevitably, your view logic will end up requiring changes to the
underlying layers, and you will write code that doesn't get used.

Instead, build vertically, column-by-column. Write code for all the vertical
layers involved in one feature before moving on to the next feature. That way,
you'll minimize rewriting, and end up with working features without waste.

A visual explanation of this suggested development workflow can be found
[here][SPA planning tips]

### Summary

The project process should look like:

- Planning: Write down your ideas (use diagrams!)
- Start by creating the frontend and backend directories
- Build the R from CRUD for just one model, vertically! That means one
  migration, one model, one controller action, one fetch call, and one DOM
  update. Add seed data and confirm that your code works by testing it visually.
- Then, build the next CRUD action (maybe Create or Update), again building
  vertically.
- Continue building features one by one, (vertically!)
- Add feature by feature, not model by model or layer by layer.
- Test each feature, add styles, and create seed data as you go (not all at once
  at the end)

### Handy Resources

- [Requirements Checklist][]
- [Javascript Project Set-Up Walkthrough][]
- [Javascript Project Rules of the Road][]
- [What To Expect In Your Project Review][]
- [draw.io][] - free online tool for creating flowcharts and diagrams

### Demo Projects

- [Beat Machine][]
- [Bounce Game][]
- [Words With Nerds™][]
- [Remixer][]
- [Keyboard Karaoke][]

[Beat Machine]: https://beat-machine.com/
[Bounce Game]: http://bounce-123.s3-website-us-east-1.amazonaws.com/
[Words With Nerds™]: https://wordswithnerds.herokuapp.com/
[Remixer]: https://remixer-v2.firebaseapp.com/
[Keyboard Karaoke]: https://keyboard-karaoke.herokuapp.com/

[draw.io]: https://www.draw.io/
[What To Expect In Your Project Review]: https://github.com/learn-co-students/js-spa-project-instructions-online-web-sp-000/blob/master/what-to-expect-in-project-reviews.md
[Javascript Project Rules of the Road]: https://github.com/learn-co-students/js-spa-project-instructions-online-web-sp-000/blob/master/project-rules-of-the-road.md
[Javascript Project Set-Up Walkthrough]: https://github.com/learn-co-students/js-spa-project-instructions-online-web-sp-000/blob/master/setup-walkthrough.md
[Requirements Checklist]: https://github.com/learn-co-students/js-spa-project-instructions-online-web-sp-000#technical-and-complexity-requirements
[SPA planning tips]: https://github.com/learn-co-students/js-spa-project-instructions-online-web-sp-000/blob/master/project-planning-tips.md
[planning form]: https://forms.gle/DhThw5wtmv3nMKmeA
[project requirements]: https://github.com/learn-co-students/js-spa-project-instructions-online-web-sp-000
[study groups]: https://learn.co/study-group
