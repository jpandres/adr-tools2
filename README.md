# ADR Tools 2
<p><a href=""><img src="https://img.shields.io/badge/ADRs-10-ff69b4" alt="Number of ADRs in this repo" /></a></p>
![example workflow](https://github.com/jpandres/adr-tools2/actions/workflows/main/badge.svg)

A command-line tool for working with a log of [Architecture Decision Records][ADRs] (ADRs).


## Quick Start


[Install ADR Tools 2](INSTALL.md).

Use the `adr` command to manage ADRs.  Try running `adr help`.

ADRs are stored in a subdirectory of your project as Markdown files.
The default directory is `doc/adr`, but you can specify the directory
when you initialise the ADR log.

1. Create an ADR directory in the root of your project:

        adr init doc/architecture/decisions

   This will create a directory named `doc/architecture/decisions`
   containing the first ADR, which records that you are using ADRs
   to record architectural decisions and links to
   [Michael Nygard's article on the subject][ADRs].

2. Create Architecture Decision Records

        adr new Implement as Unix shell scripts

   This will create a new, numbered ADR file and open it in your
   editor of choice (as specified by the VISUAL or EDITOR environment
   variable).

   To create a new ADR that supersedes a previous one (ADR 9, for example),
   use the -s option.

        adr new -s 9 Use Rust for performance-critical functionality

   This will create a new ADR file that is flagged as superseding
   ADR 9, and changes the status of ADR 9 to indicate that it is
   superseded by the new ADR.  It then opens the new ADR in your
   editor of choice.

3.  Configure the template.

        export ADR_TEMPLATE=<path to file>

4. For further information, use the built-in help:

        adr help

See the [tests](tests/) for detailed examples.

The decisions for this tool are recorded as [architecture decision records in the project repository](doc/adr/).

You can see them in HTML format at: https://jpandres.github.io/adr-tools2/ (generated with [adr-viewer](https://github.com/mrwilson/adr-viewer))

[ADRs]: https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions
