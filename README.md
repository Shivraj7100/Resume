# Shivraj_Resume
overleaf, latexeditor: Code:-
\documentclass[10pt, letterpaper]{article}

% Packages:
\usepackage[
    ignoreheadfoot, % set margins without considering header and footer
    top=2 cm, % seperation between body and page edge from the top
    bottom=2 cm, % seperation between body and page edge from the bottom
    left=2 cm, % seperation between body and page edge from the left
    right=2 cm, % seperation between body and page edge from the right
    footskip=1.0 cm, % seperation between body and footer
    % showframe % for debugging 
]{geometry} % for adjusting page geometry
\usepackage{titlesec} % for customizing section titles
\usepackage{tabularx} % for making tables with fixed width columns
\usepackage{array} % tabularx requires this
\usepackage[dvipsnames]{xcolor} % for coloring text
\definecolor{primaryColor}{RGB}{0, 0, 0} % define primary color
\usepackage{enumitem} % for customizing lists
\usepackage{fontawesome5} % for using icons
\usepackage{amsmath} % for math
\usepackage[
    pdftitle={Shivraj_jadhav_Resume},
    pdfauthor={Shivraj_jadhav_Resume},
    pdfcreator={overleaf},
    colorlinks=true,
    urlcolor=primaryColor
]{hyperref} % for links, metadata and bookmarks
\usepackage[pscoord]{eso-pic} % for floating text on the page
\usepackage{calc} % for calculating lengths
\usepackage{bookmark} % for bookmarks
\usepackage{lastpage} % for getting the total number of pages
\usepackage{changepage} % for one column entries (adjustwidth environment)
\usepackage{paracol} % for two and three column entries
\usepackage{ifthen} % for conditional statements
\usepackage{needspace} % for avoiding page brake right after the section title
\usepackage{iftex} % check if engine is pdflatex, xetex or luatex

% Ensure that generate pdf is machine readable/ATS parsable:
\ifPDFTeX
    \input{glyphtounicode}
    \pdfgentounicode=1
    \usepackage[T1]{fontenc}
    \usepackage[utf8]{inputenc}
    \usepackage{lmodern}
\fi

\usepackage{charter}

% Some settings:
\raggedright
\AtBeginEnvironment{adjustwidth}{\partopsep0pt} % remove space before adjustwidth environment
\pagestyle{empty} % no header or footer
\setcounter{secnumdepth}{0} % no section numbering
\setlength{\parindent}{0pt} % no indentation
\setlength{\topskip}{0pt} % no top skip
\setlength{\columnsep}{0.15cm} % set column seperation
\pagenumbering{gobble} % no page numbering

\titleformat{\section}{\needspace{4\baselineskip}\bfseries\large}{}{0pt}{}[\vspace{1pt}\titlerule]

\titlespacing{\section}{
    % left space:
    -1pt
}{
    % top space:
    0.3 cm
}{
    % bottom space:
    0.2 cm
} % section title spacing

\renewcommand\labelitemi{$\vcenter{\hbox{\small$\bullet$}}$} % custom bullet points
\newenvironment{highlights}{
    \begin{itemize}[
        topsep=0.10 cm,
        parsep=0.10 cm,
        partopsep=0pt,
        itemsep=0pt,
        leftmargin=0 cm + 10pt
    ]
}{
    \end{itemize}
} % new environment for highlights


\newenvironment{highlightsforbulletentries}{
    \begin{itemize}[
        topsep=0.10 cm,
        parsep=0.10 cm,
        partopsep=0pt,
        itemsep=0pt,
        leftmargin=10pt
    ]
}{
    \end{itemize}
} % new environment for highlights for bullet entries

\newenvironment{onecolentry}{
    \begin{adjustwidth}{
        0 cm + 0.00001 cm
    }{
        0 cm + 0.00001 cm
    }
}{
    \end{adjustwidth}
} % new environment for one column entries

\newenvironment{twocolentry}[2][]{
    \onecolentry
    \def\secondColumn{#2}
    \setcolumnwidth{\fill, 4.5 cm}
    \begin{paracol}{2}
}{
    \switchcolumn \raggedleft \secondColumn
    \end{paracol}
    \endonecolentry
} % new environment for two column entries

\newenvironment{threecolentry}[3][]{
    \onecolentry
    \def\thirdColumn{#3}
    \setcolumnwidth{, \fill, 4.5 cm}
    \begin{paracol}{3}
    {\raggedright #2} \switchcolumn
}{
    \switchcolumn \raggedleft \thirdColumn
    \end{paracol}
    \endonecolentry
} % new environment for three column entries

\newenvironment{header}{
    \setlength{\topsep}{0pt}\par\kern\topsep\centering\linespread{1.5}
}{
    \par\kern\topsep
} % new environment for the header

\newcommand{\placelastupdatedtext}{% \placetextbox{<horizontal pos>}{<vertical pos>}{<stuff>}
  \AddToShipoutPictureFG*{% Add <stuff> to current page foreground
    \put(
        \LenToUnit{\paperwidth-2 cm-0 cm+0.05cm},
        \LenToUnit{\paperheight-1.0 cm}
    ){\vtop{{\null}\makebox[0pt][c]{
        \small\color{gray}\textit{Last updated in September 2024}\hspace{\widthof{Last updated in September 2024}}
    }}}%
  }%
}%

% save the original href command in a new command:
\let\hrefWithoutArrow\href

% new command for external links:


\begin{document}
    \newcommand{\AND}{\unskip
        \cleaders\copy\ANDbox\hskip\wd\ANDbox
        \ignorespaces
    }
    \newsavebox\ANDbox
    \sbox\ANDbox{$|$}

    \begin{header}
        \fontsize{25 pt}{25 pt}\selectfont Shivraj Jadhav

        \vspace{5 pt}

        \normalsize
        \mbox{Pune, Maharashtra}%
        \kern 5.0 pt%
        \AND%
        \kern 5.0 pt%
        \mbox{\hrefWithoutArrow{mailto:shivrajjadhav710@gmail.com}{shivrajjadhav710@gmail.com}}%
        \kern 5.0 pt%
        \AND%
        \kern 5.0 pt%
        \mbox{\hrefWithoutArrow{+91 8788349062}{8788349062}}%
        \kern 5.0 pt%
        \AND%
        \kern 5.0 pt%
        \mbox{\hrefWithoutArrow{https://linkedin.com/in/shivrajjadhav}{linkedin.com/in/shivrajjadhav}}%
        \kern 5.0 pt%
        \AND%
        \kern 5.0 pt%
        \mbox{\hrefWithoutArrow{https://github.com/shivraj7100}{github.com/shivraj7100}}%
    \end{header}

    \vspace{10 pt - 0.3 cm}

        \begin{bold}
            
        \begin{center}
            
            
            \href{https://rendercv.com} Data Analyst and Data Science Enthusiast Data visualization to extract actionable insights and drive decision making.}.
      \end{center}}
       \end{bold}
        \vspace{0.2 cm}
           

    \section{Education}        
        \begin{twocolentry}{
            [2022 – 2025]
        }
            \textbf{G H Raisoni College Of Engineering And Management Wagholi, Pune | SPPU | B.Tech(Data Science)}\end{twocolentry}

        \vspace{0.10 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item  CGPA: 7.78 /10.0 )
            \end{highlights}
        \end{onecolentry} 

     \begin{twocolentry}{
            [2021 – 2022]
        }
            \textbf{ TMC, Ichalkarnji Maharashtra | Shivaji University Kolhapur| HSC(PCM)}\end{twocolentry}

        \vspace{0.10 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item  Marks: 91.84 /100.0 )
            \end{highlights}
        \end{onecolentry}
    
     \begin{twocolentry}{
            [2018 – 2019]
        }
            \textbf{ Uttareshwar High School, Vidani, Phaltan | SSC}\end{twocolentry}

        \vspace{0.10 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item  Marks: 71.60 /100.0 )
            \end{highlights}
        \end{onecolentry}
    
    
    

    
    \section{Projects}

        
        \begin{twocolentry}{
            \href{https://github.com/shivraj7100}{[GitHub]}
        }
            \textbf{A Web Application for the Analysis of Olympic Dataset }\end{twocolentry}

        \vspace{0.10 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item A Web Application: Olympic data set analysis.
             It is a stream lit framework-based project, Main objective of this project is analyzing of historical • Olympic dataset and this makes it easier to gain crucial insights from historical dataset.

                \item  Tech Stack: Python, Stream lit, Marplotlib, Pandas, etc.
            \end{highlights}
        \end{onecolentry}


        \vspace{0.2 cm}

        \begin{twocolentry}{
            \href{https://github.com/shivraj7100}{[GitHub]}
        }
            \textbf{Ecommerce Sales Dashbord}\end{twocolentry}

        \vspace{0.10 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item a visual interface that helps store owners, managers, and marketers track and analyze the performance of their
                 e-commerce operations.
                \item Tech stack:- Power-BI \end{highlights} \end{onecolentry}


        \vspace{0.2 cm}

        \begin{twocolentry}{
             \href{https://github.com/shivraj7100}{[GitHub]}
        }
            \textbf{ATM-Transaction-Analysis-Dashboard}\end{twocolentry}

        \vspace{0.10 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item Analyze transaction as well as performance maintenance of atm and it is state wise analysis
                \item Tech Stack:- Power-BI
            \end{highlights}
        \end{onecolentry}

 \section{Publications}

        
        \begin{samepage}
            \begin{twocolentry}{
                Nov 2023
            }
                \textbf{A Stream lit web application for the analysis of Olympic dataset}
            \end{twocolentry}

            \vspace{0.10 cm}
            
            \begin{onecolentry}
                \mbox{Publication:- jetir}, \mbox{\textbf{\textit{Author: Shivraj Jadhav}}}

                \vspace{0.10 cm}
                
        \href{https://www.jetir.org/view?paper=JETIR2311414}{(Research-Paper)}
        \end{onecolentry}
        \end{samepage}

    
    \section{Technologies}
     
        \begin{onecolentry}
            \textbf{Programming Languages:} Python, HTML, CSS, SQL \end{onecolentry}
        \vspace{0.2 cm}

          \begin{onecolentry}
            \textbf{Data Analysis Tools:}Python, Power Bi, Excel}
            \end{onecolentry}
        \vspace{0.2 cm}
         
           \begin{onecolentry}
            \textbf{Tools:}VS Code, Jupyter Notebook, Git-Hub.}
        \end{onecolentry}
        \vspace{0.2 cm}
        
         \begin{onecolentry}
            \textbf{Frameworks:} Django, Flask.}
        \end{onecolentry}
         \vspace{0.2 cm}
        
    \section{Certifications}

        
        \begin{samepage}
            \begin{twocolentry}{
                Jan 2024
            }
                \textbf{ 1) A Joy of computing - python}  [Issued By:- NPTEL]
                \href{https://archive.nptel.ac.in/content/noc/NOC24/SEM2/Ecertificates/106/noc24-cs113/Course/NPTEL24CS113S75200242304300942.pdf}{(Certificate)}
            \end{twocolentry}

            \vspace{0.10 cm}
            
            \begin{onecolentry}
                
                \vspace{0.10 cm}
                
        \end{onecolentry}
        \end{samepage}

         
    


\end{document}

