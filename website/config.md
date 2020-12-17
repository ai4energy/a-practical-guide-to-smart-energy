<!--
Add here global page variables to use throughout your
website.
The website_* must be defined for the RSS to work
-->
@def website_title = "智慧能源实践之路"
@def website_descr = "智慧能源实践之路课程网站"
@def website_url   = "https://msoc.ai4energy.org/"

@def title         = "智慧能源实践之路"

<!-- @def prepath       = "Spring2021" -->
@def description = """智慧能源实践之路课程网站"""
@def author        = "Mingtao Li"
@def mintoclevel   = 2

<!--
Add here files or directories that should be ignored by Franklin, otherwise
these files might be copied and, if markdown, processed by Franklin which
you might not want. Indicate directories by ending the name with a `/`.
-->
@def ignore = ["node_modules/", "franklin", "franklin.pub"]

<!--
Add here global latex commands to use throughout your
pages. It can be math commands but does not need to be.
For instance:
* \newcommand{\phrase}{This is a long phrase to copy.}
-->

@def use_header_img     = true
@def use_hero           = false
@def hero_width         = "80%"
@def hero_margin_top    = "100px"

@def add_github_view  = true
@def add_github_star  = true
@def github_repo      = "ai4energy/a-practical-guide-to-smart-energy"


@def section_width = 10

@def header_color       = "#3f6388"
@def link_color         = "#2669DD"
@def link_hover_color   = "teal"
@def section_bg_color   = "#f6f8fa"
@def footer_link_color  = "cornflowerblue"

@def highlight_theme    = "atom-one-dark"
@def code_border_radius = "10px"
@def code_output_indent = "15px"


@def sections        = Pair{String,String}[]
@def section_counter = 1
@def showall         = true


\newcommand{\center}[1]{~~~<div style="text-align:center;">~~~#1~~~</div>~~~}
\newcommand{\out}[1]{@@code-output \show{#1} @@}

\newcommand{\blurb}[1]{~~~<p style="font-size: 1.15em; color: #333; line-height:1.5em">~~~#1~~~</p>~~~}

\newcommand{\R}{\mathbb R}
\newcommand{\scal}[1]{\langle #1 \rangle}
