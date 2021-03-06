#### 1. Pain Points

You should think of a couple of pain points in your life that you would like to solve with a simple CRUD app. Remember,

> The verb you want to be using with respect to startup ideas is not "think up" but "notice."
> — [Paul Graham, "How to Get Startup Ideas"][1]

Don't try to think up billion dollar startup ideas; our goal here is to discover a good first learning project, not to save the world just yet. Try to notice a real annoyance at work or at home or with friends that we can solve, even if for just one user -- you.

For example, [here is a project that a student made last quarter][2] -- a simple app that lets you keep track of whether or not it's time to dry clean pieces of clothing. Another student made a nice app that suggests which of your credit cards to use in order to maximize rewards based on what kind of purchase you are about to make.

If you want to get fancier than a simple CRUD app and incorporate some APIs to pull in external data, you are more than welcome to, but try to [do some research][3] and make sure that an API exists for what you want (e.g., live sports scores).

**The bottomline: keep it simple.** It's best to think up more than one idea if you can, so that we have options to choose from.

#### 2. Sketches

Once I have an idea in mind, I immediately reach for pen and paper and sketch out each screen in the app. Some people find it easier to start with the central, most important screen; others find it easier to walk through the user's flow chronologically, starting from sign-up.

I personally find it easiest to visualize the main, most important screen in the app first. I sketch it out. I then try to "crawl" my idea by noticing every link or button on that page, and then drawing the next screen that it would lead me to. I rinse and repeat until I've sketched out every screen.

#### 3. User Stories

We now want to write down our [User Stories][7]. User stories are just features, phrased in a particular manner:

"As a **[role]**, I want to be able to **[capability]**," (and, optionally), "so that **[benefit]**."

The aim is to always be thinking from a user-centric perspective, and not from a technology or implementation perspective yet.

First, brain-dump all the features you can possibly imagine as user stories.

**Then, re-order them by priority.** A drag-and-drop interface like Trello's, or [Atom's Move Line Up/Down keyboard shortcuts](https://github.com/nwinkler/atom-keyboard-shortcuts#editing), can be handy for this.

Then, crucially, ask yourself: **what is the absolute minimum featureset I can get away with in the prototype?** The prototype's purpose is just to validate whether or not the idea is feasible and whether the core value is actually valuable. **Be ruthless in eliminating all non-essential user stories for this first draft.**

**Cross out any delayable stories to exclude them.**

#### 4. Domain Modeling

Now that we've identified the features we want to include in our prototype, from a user's perspective, it's finally time to start thinking about how we're actually going to code it up.

The primary thing we need to do is **identify the tables and columns** we need in our database to keep track of all the information required to support the user stories. This is known as **domain modeling**. If we can get this part right, the rest of the code practically writes itself (trust me, you'll see).

My process for domain modeling is, once I have my list of actions and information on each screen, and my user stories in front of me -- try to identify the important **nouns** in the app. These usually become tables -- for example, events, recipes, tweets, users, messages, etc.

For each table, try to identify the columns we need. What are all the attributes about that thing that you need to track? For example, for events, you probably need held_on (date), title (string), description (text), location (string), etc.

Start diagramming out your domain model in [First Draft](https://ideas.firstdraft.com/).

#### Associations

The last and most crucial step in domain modeling is identifying relationships between each pair of tables.

A relationship can be one of two types: one-to-many, and many-to-many.

For example, in Instagram, a photo can be associated to many comments, but a comment can only be associated to one photo. This is a one (photo) to many (comments) association.

On the other hand, in IMDB, a movie can be associated to many actors, and an actor can also be associated to many movies. This is a many-to-many association.

The first step is, try to go through all of your tables and identify all one-to-many associations.

Once you feel good about your one-to-manies, try to identify all the important many-to-manies too.

For all one-to-manies, decide which table should get the foreign key column, and what it should be called.

For all many-to-manies, decide on a name for the join model.

Add your associations, and any required join models and foreign keys, to your [diagram in First Draft](https://ideas.firstdraft.com/).

**You should now have a complete listing of all your tables and columns, including those needed to support your associations.**

**Once you've taken a stab at writing down your domain model, it's time to book an appointment with one of us to review it.** The more progress you make on your own with domain modeling, the more productive our chat will be.

### Have fun!

P.S. The domain modeling tool is under active development. You can test out experimental code generation functionality by clicking "Publish". Come back in a few minutes and refresh, and you should see buttons that lead to some code on GitHub and a prototype on Heroku. The hope is that by clicking through the prototype and entering some data, you will catch flaws in your domain model and can then go back and update your diagram. Please feel free to send us any and all feedback.

[1]: http://paulgraham.com/startupideas.html
[2]: https://www.youtube.com/watch?v=U5fdaaZWwaY&feature=youtu.be
[3]: http://www.programmableweb.com/apis/directory
[4]: http://www.firstdraft.com/
[5]: https://signalvnoise.com/posts/1880-the-different-sketch-styles-of-the-designers-at-37signals/
[6]: https://balsamiq.com/
[7]: https://www.mountaingoatsoftware.com/agile/user-stories
[8]: https://gist.github.com/rbetina/80d3cf2cf82666ed1c0f
[9]: https://rbetina.youcanbook.me/
[10]: https://plus.google.com/hangouts/_/g3phohfi7pq5dlfq6zhhfkjsiua
[11]: http://www.firstdraft.com/ideas
[12]: http://ask.firstdraft.com/t/first-draft-ideas-feedback/346