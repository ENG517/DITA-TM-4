# DITA Topic Model - Using and Maintaining a 1950's Portable Manual Smith Corona Typewriter

This repo contains a DITA topic model (TM) related to the necessary steps to use, maintain, and repair a 1950's Portable Manual Smith Corona Typewriter. 

## Authors

- Harshini Ravindran
- Gabby Simon
- Alli Wray

## Project Maps

### User Scenario 1: Beginner User

A first-time typewriter user, Genesis, has just purchased her very first typewriter. She wants to start using her typewriter for creative writing, but she has never set up a typewriter for use before, and doesn’t know where to begin. She needs to learn how to load paper into her machine, and how to format the paper before she begins typing.

Map Outline:
- c_filename.dita (File title)
- c_filename.dita (File title)
- t_filename.dita (File title)
  - t_filename.dita (File title)

### User Scenario 2: Intermediate User

An intermediate typewriter user, Park, is writing their debut novel on their vintage typewriter. They have written an extensive amount of text and have noticed that their typewriter is running low on ink, has an overall low performance, and is getting a bit dirty. They would like to continue using their typewriter, but they are relatively inexperienced in typewriter maintenance, and need to know how to clean the typewriter and perform some minor repairs.

Map Outline:
- c_filename.dita (File title)
- c_filename.dita (File title)
- t_filename.dita (File title)
  - t_filename.dita (File title)

### User Scenario 3: Advanced User

An advanced typewriter user, Hunter, has recently purchased a 1957 Smith Corona Manual typewriter to restore for long term use in creative writing. He wants to know the appropriate steps and materials to complete a full restoration of the interior, exterior, and casing of the typewriter.

Map Outline:
- c_filename.dita (File title)
- c_filename.dita (File title)
- t_filename.dita (File title)
  - t_filename.dita (File title)

## Folders &amp; Files

- `assets`: Contains all assets used within the TM.
- `concepts`: Contains all concept topics.
- `references`: Contains all reference topics.
- `tasks`: Contains all task topics.
- `shared`: Contains all topic files that are shared across multiple maps.
- `out`: Contains all output folders.
- `themes`: Contains `.yaml` style configuration files.
- **Skeleton files**: All topic folders contain a single "skeleton" topic file for you to copy, whenever you need to quickly create a new file.
- `.keep` **files**: Ignore these files. They ensure that any empty folders are tracked by git. 
- `.gitignore`: This file tells git which files to ignore in the repo. You can leave this one be.

## Filenaming Conventions

- Task Topics: `t_verb_verbobject.dita`
- Concept Topics: `c_nounphrase.dita`
- Reference Topics: It varies, but something akin to `r_types_of_nounphrase.dita`
- Dita Maps: `_modelname.ditamap`

## Building Outputs Manually with the Command Line

See the DITA-OT user guide about how to generate output: [https://www.dita-ot.org/dev/topics/build-using-dita-command](https://www.dita-ot.org/dev/topics/build-using-dita-command)

### Sample DITA Commands

#### Help

To see all of the commands and parameters, use the following command:

```
dita --help
```

#### DITA options and arguments

```
-f == dita output format
-i == dita input map file
-o == dita output directory
-D&lt;property&gt;=&lt;value&gt; == add custom args
    with particular values to dita transformation
-filter &lt;file&gt; == filter and flagging file
```

#### Create an HTML5 site

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```

#### Create an HTML5 site with a custom CSS file

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
  -Dargs.cssroot='url/to/your/assets/folder' \
  -Dargs.css='${cssroot}/your-custom-css-file.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
```

#### Create a PDF

```
dita -f pdf -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```
