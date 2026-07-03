%figures:

\begin{figure}[h]
\centering
\begin{subfigure}{0.45\textwidth}
\centering
\begin{tikzpicture}
\draw[->] (0,0) -- (2,0);
\draw[->] (0,0) -- (0,2);
\end{tikzpicture}
\caption{Axes}
\end{subfigure}
\hfill
\begin{subfigure}{0.45\textwidth}
\centering
\includegraphics[width=\linewidth]{example-image}
\caption{Image}
\end{subfigure}
\caption{Example figure with TikZ and subcaption}
\end{figure}

\documentclass[10pt,twoside]{book}

%\baselineskip 16pt \oddsidemargin 10pt \evensidemargin 10pt 
%\topmargin 0pt \headheight 0pt \headsep 0pt \footskip 32pt 
%\textheight 40\baselineskip \advance \textheight by \topskip 
%\textwidth 455pt
%\setlength{\headheight}{26pt} 


\usepackage[lmargin=40pt,rmargin=40pt,tmargin=70pt,bmargin=60pt,headheight=26pt]{geometry}

\usepackage{setspace}
\onehalfspacing % or \doublespacing

%\usepackage{auto-pst-pdf}

\usepackage{extarrows}
\usepackage{amsmath,amssymb,amsfonts,amsthm,MnSymbol,mathtools}
\usepackage{underoverlap}
\usepackage{latexsym}
\usepackage{graphicx}
\usepackage[hidelinks,unicode,psdextra]{hyperref}
\usepackage{chngcntr}
\usepackage{multirow}
\setcounter{MaxMatrixCols}{16}
\usepackage{braket}
\usepackage{float}
\usepackage{enumerate}
\usepackage{bbm}
\usepackage{blkarray}
\usepackage{tensor}
\usepackage{tikz}

\usepackage{appendix}

\usepackage[notlof,notlot,nottoc]{tocbibind}
%\usepackage[notlot,nottoc]{tocbibind}

\usepackage{makeidx}
\makeindex

\usepackage{empheq}

\usepackage{fancyhdr} 
\pagestyle{fancy}
\fancyhead{}
%\fancyhead[LE,RO]{\thepage}

\fancyhead[LE]{\leftmark}
\fancyhead[RO]{\rightmark}

%\renewcommand{\chaptermark}[1]{%
%\markboth{\MakeUppercase{#1}}{}}

%\renewcommand{\chaptermark}[1]{%
%\markboth{\thechapter.\ \MakeUppercase{#1}}{}}

\makeatletter
\renewcommand{\chaptermark}[1]{%
  \markboth{\thechapter.\ \MakeUppercase{#1}}{\MakeUppercase{%
    \ifnum\c@secnumdepth>\m@ne \thechapter. \ \fi #1}}%
} 
\makeatother


\renewcommand{\sectionmark}[1]{\markright{\thesection.\ #1}}

\makeatletter
\def\cleardoublepage{\clearpage\if@twoside \ifodd\c@page\else
\hbox{}
%\vspace*{\fill}
%\begin{center}
%This page intentionally contains only this sentence.
%\end{center}
%\vspace{\fill}
\thispagestyle{empty}
\newpage
%\if@twocolumn\hbox{}\newpage\fi
\fi\fi}
\makeatother




\setcounter{secnumdepth}{2}

\setcounter{tocdepth}{2}

\newcommand{\sgn}{\text{sgn}}

\newcommand{\md}{\mathrm{d}}
 
 \newcommand{\Fd}{ { \mathbbm{d} }}

\newcommand{\pq}{{\pmb q}}
\newcommand{\pvph}{{\pmb \varphi}}
\newcommand{\pph}{{\pmb \phi}}
\newcommand{\pps}{{\pmb \psi}}
\newcommand{\ppi}{{\pmb \pi}}
\newcommand{\pp}{{\pmb p}}
\newcommand{\pe}{{\pmb \epsilon}}
 
\newcommand{\vp}{\mathbf{p}}
\newcommand{\vq}{\mathbf{q}}
\newcommand{\vk}{\mathbf{k}}
\newcommand{\vx}{\mathbf{x}}
\newcommand{\vy}{\mathbf{y}}
\newcommand{\vz}{\mathbf{z}}
\newcommand{\vs}{\mathbf{s}}
 
\newcommand{\cA}{{\cal{A}}}
\newcommand{\cB}{{\cal{B}}}
\newcommand{\cC}{{\cal{C}}}
\newcommand{\cD}{{\cal{D}}}
\newcommand{\cE}{{\cal{E}}}
\newcommand{\cF}{{\cal{F}}}
\newcommand{\cG}{{\cal{G}}}
\newcommand{\cH}{{\cal{H}}}
\newcommand{\cJ}{{\cal{J}}}
\newcommand{\cI}{{\cal{I}}}
\newcommand{\cK}{{\cal{K}}}
\newcommand{\cL}{{\cal{L}}}
\newcommand{\cM}{{\cal{M}}}
\newcommand{\cO}{{\cal{O}}}
\newcommand{\cP}{{\cal{P}}}
\newcommand{\cQ}{{\cal{Q}}}
\newcommand{\cR}{{\cal{R}}}
\newcommand{\cS}{{\cal S}}
\newcommand{\cT}{{\cal{T}}}
\newcommand{\cV}{{\cal{V}}}
\newcommand{\cW}{{\cal W}}

\newcommand{\cU}{{\cal{U}}}

\newcommand{\mF}{\mathfrak{F}}
\newcommand{\mT}{\mathfrak{T}}
\newcommand{\mM}{\mathfrak{M}}

\newcommand{\mbM}{\mathbb{M}}
\newcommand{\mbT}{\mathbb{T}}
 
 \newcommand{\tvp}{ {\tilde \varphi} } 
\newcommand{\tx}{ {\tilde x} }
\newcommand{\tp}{ {\tilde p} }
\newcommand{\ty}{ {\tilde y} }
\newcommand{\tz}{ {\tilde z} }
\newcommand{\tir}{ {\tilde r} }
\newcommand{\tih}{ {\tilde h} }
\newcommand{\tic}{ {\tilde c} }
\newcommand{\tG}{ \tilde \Gamma}
 
\newcommand{\tO}{ \tilde{O}}

\newcommand{\wtD}{\widetilde{\Delta}}
 
\newcommand{\da}[1]{\mathfrak{da}{[#1]}}
\documentclass[10pt,twoside]{book}

%\baselineskip 16pt \oddsidemargin 10pt \evensidemargin 10pt 
%\topmargin 0pt \headheight 0pt \headsep 0pt \footskip 32pt 
%\textheight 40\baselineskip \advance \textheight by \topskip 
%\textwidth 455pt
%\setlength{\headheight}{26pt} 


\usepackage{bbm}

\usepackage[lmargin=40pt,rmargin=40pt,tmargin=70pt,bmargin=60pt,headheight=26pt]{geometry}

\usepackage{setspace}
\onehalfspacing % or \doublespacing

%\usepackage{auto-pst-pdf}

\usepackage{extarrows}
\usepackage{amsmath,amssymb,amsfonts,amsthm,MnSymbol,mathtools}
\usepackage{underoverlap} 
\usepackage{graphics,subfigure,color} 
\usepackage{latexsym}
\usepackage[dvips]{graphicx}
\usepackage{epsfig}
\usepackage[hidelinks,unicode,psdextra]{hyperref}
\usepackage{chngcntr}
\usepackage{psfrag}
\usepackage{multirow}
\setcounter{MaxMatrixCols}{16}
\usepackage{braket}
\usepackage{float}
\usepackage{enumerate}
\usepackage{bbm}
\usepackage{blkarray}
\usepackage{tensor}
\usepackage{tikz}

\usepackage{appendix}

\usepackage[notlof,notlot,nottoc]{tocbibind}
%\usepackage[notlot,nottoc]{tocbibind}

\usepackage{makeidx}
\makeindex

\usepackage{empheq}

\usepackage{fancyhdr} 
\pagestyle{fancy}
\fancyhead{}
%\fancyhead[LE,RO]{\thepage}

\fancyhead[LE]{\leftmark}
\fancyhead[RO]{\rightmark}

%\renewcommand{\chaptermark}[1]{%
%\markboth{\MakeUppercase{#1}}{}}

%\renewcommand{\chaptermark}[1]{%
%\markboth{\thechapter.\ \MakeUppercase{#1}}{}}

\makeatletter
\renewcommand{\chaptermark}[1]{%
  \markboth{\thechapter.\ \MakeUppercase{#1}}{\MakeUppercase{%
    \ifnum\c@secnumdepth>\m@ne \thechapter. \ \fi #1}}%
} 
\makeatother


\renewcommand{\sectionmark}[1]{\markright{\thesection.\ #1}}

\makeatletter
\def\cleardoublepage{\clearpage\if@twoside \ifodd\c@page\else
\hbox{}
%\vspace*{\fill}
%\begin{center}
%This page intentionally contains only this sentence.
%\end{center}
%\vspace{\fill}
\thispagestyle{empty}
\newpage
%\if@twocolumn\hbox{}\newpage\fi
\fi\fi}
\makeatother




\setcounter{secnumdepth}{2}

\setcounter{tocdepth}{2}

\newcommand{\sgn}{\text{sgn}}

\newcommand{\md}{\mathrm{d}}
 
 \newcommand{\Fd}{ { \mathbbm{d} }}

\newcommand{\pq}{{\pmb q}}
\newcommand{\pvph}{{\pmb \varphi}}
\newcommand{\pph}{{\pmb \phi}}
\newcommand{\pps}{{\pmb \psi}}
\newcommand{\ppi}{{\pmb \pi}}
\newcommand{\pp}{{\pmb p}}
\newcommand{\pe}{{\pmb \epsilon}}
 
\newcommand{\vp}{\mathbf{p}}
\newcommand{\vq}{\mathbf{q}}
\newcommand{\vk}{\mathbf{k}}
\newcommand{\vx}{\mathbf{x}}
\newcommand{\vy}{\mathbf{y}}
\newcommand{\vz}{\mathbf{z}}
\newcommand{\vs}{\mathbf{s}}
 
\newcommand{\cA}{{\cal{A}}}
\newcommand{\cB}{{\cal{B}}}
\newcommand{\cC}{{\cal{C}}}
\newcommand{\cD}{{\cal{D}}}
\newcommand{\cE}{{\cal{E}}}
\newcommand{\cF}{{\cal{F}}}
\newcommand{\cG}{{\cal{G}}}
\newcommand{\cH}{{\cal{H}}}
\newcommand{\cJ}{{\cal{J}}}
\newcommand{\cI}{{\cal{I}}}
\newcommand{\cK}{{\cal{K}}}
\newcommand{\cL}{{\cal{L}}}
\newcommand{\cM}{{\cal{M}}}
\newcommand{\cO}{{\cal{O}}}
\newcommand{\cP}{{\cal{P}}}
\newcommand{\cQ}{{\cal{Q}}}
\newcommand{\cR}{{\cal{R}}}
\newcommand{\cS}{{\cal S}}
\newcommand{\cT}{{\cal{T}}}
\newcommand{\cV}{{\cal{V}}}
\newcommand{\cW}{{\cal W}}

\newcommand{\cU}{{\cal{U}}}

\newcommand{\mF}{\mathfrak{F}}
\newcommand{\mT}{\mathfrak{T}}
\newcommand{\mM}{\mathfrak{M}}

\newcommand{\mbM}{\mathbb{M}}
\newcommand{\mbT}{\mathbb{T}}
 
 \newcommand{\tvp}{ {\tilde \varphi} } 
\newcommand{\tx}{ {\tilde x} }
\newcommand{\tp}{ {\tilde p} }
\newcommand{\ty}{ {\tilde y} }
\newcommand{\tz}{ {\tilde z} }
\newcommand{\tir}{ {\tilde r} }
\newcommand{\tih}{ {\tilde h} }
\newcommand{\tic}{ {\tilde c} }
\newcommand{\tG}{ \tilde \Gamma}
 
\newcommand{\tO}{ \tilde{O}}

\newcommand{\wtD}{\widetilde{\Delta}}
 
\newcommand{\da}[1]{\mathfrak{da}{[#1]}}

% Want to eliminate all these 
\newcommand{\be}{\begin{equation}}
\newcommand{\ee}{\end{equation}}
\newcommand{\nn}{\nonumber}
\newcommand{\f}{\frac}
\newcommand{\p}{\partial}
\newcommand{\na}{\nabla}
%\newcommand{\Tr}{{\rm Tr}}
\newcommand{\tr}{{\rm tr}}
\newcommand{\STr}{{\rm STr}}
\newcommand{\la}{\langle}
\newcommand{\ra}{\rangle}
\newcommand{\bfa}{\mathbf{a}}
\newcommand{\bfb}{\mathbf{b}}
\newcommand{\bfc}{\mathbf{c}}
\newcommand{\bfd}{\mathbf{d}}
\newcommand{\bfe}{\mathbf{e}}
\newcommand{\bff}{\mathbf{f}}
\newcommand{\bfm}{\mathbf{m}}
\newcommand{\bfn}{\mathbf{n}}


\let\a=\alpha \let\b=\beta  \let\g=\gamma  \let\d=\delta
\let\z=\zeta  \let\h=\eta   \let\th=\theta \let\vth=\vartheta \let\k=\kappa \let\l=\lambda
\let\m=\mu    \let\n=\nu    \let\x=\xi      \let\r=\rho \let\om=\omega
\let\s=\sigma \let\t=\tau   \let\vph=\varphi
  \let\y=\upsilon  \let\si=\varsigma
\let\D=\Delta  \let\Th=\Theta \let\L=\Lambda \let\Om=\Omega

\let\vph=\varphi
\let\vphi=\varphi
\let\d=\delta
\let\G=\Gamma 
\newcommand{\uG}{\underline{G}}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


\DeclareMathOperator{\Tr}{Tr}
\DeclareMathOperator{\Det}{Det}

\newtheorem{definition}{Definition}[chapter]
\newtheorem{proposition}{Proposition}[chapter]
\newtheorem{lemma}{Lemma}[chapter]
\newtheorem{construction}{Construction}[chapter]
\newtheorem{theorem}{Theorem}[chapter]
\newtheorem{conjecture}{Conjecture}[chapter]
\newtheorem{corollary}{Corollary}[chapter]
\newtheorem{axiom}{Axiom}[chapter]

%\theoremstyle{definition}
\newtheorem{remark}{Remark}[chapter]
\newtheorem{example}{Example}[chapter]
\newtheorem{exercise}{Exercise}[chapter]

\newtheorem{question}{Question}
\newtheorem{answer}{Answer}

\renewcommand{\thefigure}{\arabic{chapter}.\arabic{figure}}

\renewcommand{\thefootnote}{\arabic{footnote}}

\renewcommand{\theequation}{\arabic{chapter}.\arabic{equation}}

\renewcommand{\thedefinition}{\arabic{chapter}.\arabic{definition}}

\renewcommand{\theproposition}{\arabic{chapter}.\arabic{proposition}}

\renewcommand{\thelemma}{\arabic{chapter}.\arabic{lemma}}

\renewcommand{\thetheorem}{\arabic{chapter}.\arabic{theorem}}

\renewcommand{\theconjecture}{\arabic{chapter}.\arabic{conjecture}}

\renewcommand{\theconstruction}{\arabic{chapter}.\arabic{construction}}

\renewcommand{\thecorollary}{\arabic{chapter}.\arabic{corollary}}

\renewcommand{\theremark}{\arabic{chapter}.\arabic{remark}}

\renewcommand{\theexample}{\arabic{chapter}.\arabic{example}}

\renewcommand{\theexercise}{\arabic{chapter}.\arabic{exercise}}

\definecolor{bluegray}{rgb}{0.4, 0.6, 0.8} 
\definecolor{brickred}{rgb}{0.8, 0.25, 0.33}
\definecolor{brightcerulean}{rgb}{0.11, 0.67, 0.84}
\definecolor{celestialblue}{rgb}{0.29, 0.59, 0.82}
\definecolor{darkpastelblue}{rgb}{0.47, 0.62, 0.8}
\definecolor{iceberg}{rgb}{0.44, 0.65, 0.82}
\definecolor{lightcornflowerblue}{rgb}{0.6, 0.81, 0.93}
\definecolor{lightskyblue}{rgb}{0.53, 0.81, 0.98}
\definecolor{palecornflowerblue}{rgb}{0.67, 0.8, 0.94}
\definecolor{britishracinggreen}{rgb}{0.0, 0.26, 0.15}
\definecolor{auburn}{rgb}{0.43, 0.21, 0.1}
\definecolor{bulgarianrose}{rgb}{0.28, 0.02, 0.03}
\definecolor{darkgreen}{rgb}{0.0, 0.2, 0.13}



\allowdisplaybreaks[4]

%\bibliographystyle{amsplain}

%\usepackage[backend=bibtex,bibstyle=trad-unsrt,doi=false,isbn=false,url=false,sorting=nyt]{biblatex}
\usepackage[backend=bibtex,bibstyle=ieee,doi=false,isbn=false,url=false,sorting=nyt]{biblatex}
\addbibresource{Refs.bib}

%\addbibresource{~/Desktop/lucru/Ongoing/Refs/Refs.bib}

\DeclareFieldFormat[article,inproceedings,book]{title}{\textit{#1}}
\DeclareFieldFormat[inproceedings]{booktitle}{{#1}}
\AtBeginBibliography{\renewcommand\finalandcomma{}}
\DeclareFieldFormat[article]{journaltitle}{\text{#1}}
%\DeclareFieldFormat[article]{volume}{\textbf{#1}}

%\DeclareFieldFormat[article]{pages}{ \text{#1}}
%\DeclareFieldFormat[article]{number}{}
%\DeclareFieldFormat[book]{volume}{}


\vbadness=9999
\tolerance=9999
\clubpenalty=10000
\widowpenalty=10000


\newlength{\drop} 

\newcommand*{\titleM}{\begingroup 
\drop = 0.08\textheight
\centering
\vspace*{\drop}
{\Huge\bfseries full title}\par
\vspace*{2\drop}
{\Large\scshape name}\par
\vspace*{2\drop}
{\scshape 

institute
}
\par
\vfill

\endgroup}
 

\makeatletter
\def\blfootnote{\xdef\@thefnmark{}\@footnotetext}
\makeatother

\begin{document}

%\thispagestyle{empty}

%\titleM

 
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%\newpage


%\thispagestyle{empty}

%${}$

%\newpage

\renewcommand{\thepage}{\roman{page}}

\setcounter{page}{1}

\thispagestyle{empty}

\titleM

%\dedicatie


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\cleardoublepage

\tableofcontents


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\cleardoublepage

\renewcommand{\thepage}{\arabic{page}}

\setcounter{page}{1}

%\part{H\"oMa I}

\chapter{Introduction}
 \emph{Axioms} are statements which are accepted to be true. 
 \emph{Theorems} (lemmatas, propositions, etc.) are statements that can be proven using logical reasoning starting from axioms. We know since the work of G\"odel that no system of axioms is complete, that is for any system of axioms which includes the natural numbers it is possible to formulate statements that are undecidable, that is can neither be proved true nor be proven false . This is because, essentially, there are more possible statements that can be formulated than there are possible proofs.
 
\emph{Reductio ad absurdum} is a strategy of proving a statement is true by first assuming the statement is false and proving that this implies a contradiction (i.e. some other false statement). As a true statement can not imply a false one, one concludes that the original statement is true. 

\emph{Mathematical induction} is a strategy of proving a statement indexed by a natural number $n$ is true by first proving it is true for $n=0$ and then proving that if the statement for $n$ is true then the one for $n+1$ is also true. Transfinite induction is indexed by ordinal numbers in stead of natural ones.

The following logic symbols are useful $\exists, !,\forall, \Rightarrow, \Leftrightarrow, =$. We denote $\equiv$ when the left hand side and the right hand side are equal by definition.


\part{H\"oMa I}

\chapter{Sets and numbers}
 
%\input{Preliminaries}
 
\chapter{Topological spaces}
  \label{ch:topo}

\input{TopoSpaces}

\chapter{Sequences}
\label{ch:sequences}

%\input{Sequences}
      
\chapter{Vector spaces, first contact}
\label{ch:FDVecspaces}
%\input{FDVecspaces}

\chapter{Matrices}

%\input{LinAl}


\chapter{Functions, first contact}
\label{ch:Rfunctions}

%\input{RFunctions}

\part{H\"oMa II}

\chapter{Spectral theory in finite dimensions}

%\input{Eigenvalues}

\chapter{Banach spaces}

\label{ch:vecBanach}
%\input{BVecspaces}
       
\chapter{Functions}
\label{ch:functions}

%\input{Functions}

 \chapter{The Riemann integral}
 \label{ch:integral}

%\input{SmoothInt}

\chapter{Elements of differential geometry}

% \input{DiffGeom}

\chapter{The Stokes theorem}

%\input{Stokes}

 \part{H\"oMa III}
   
 \chapter{Complex analysis}
  
% \input{ComplexAnalysis}

\chapter{Hilbert spaces \texttt{(Hilbert Raum)}} 
 \label{ch:HVecspaces}
 
%  \input{HVecspaces}
 
\chapter{The Lebesgue integral, first contact}
  \label{ch:Lebesgue}
 
% \input{Integration}
 
 \chapter{The Fourier transform}
 
%\input{FT}

 
 \chapter{Distributions}
   \label{ch:Distributions}
   
%\input{Distributions}

 
\chapter{Differential equations}
\label{ch:ODE}
%\input{ODE}


\appendix

\appendixpage
\noappendicestocpagenum
\addappheadtotoc

\chapter{Lie groups and representations, a primer}

%\input{MatrixGroups}

%\chapter{Elements of probability and statistics}

%\input{Proba}

%\chapter{Special functions}

%\input{Trigo}

\chapter{Exams}

%\input{Exams}



 
\cleardoublepage

\begingroup
\sloppy
\printbibliography[heading=bibintoc]
\endgroup


\end{document}

% Want to eliminate all these 
\newcommand{\be}{\begin{equation}}
\newcommand{\ee}{\end{equation}}
\newcommand{\nn}{\nonumber}
\newcommand{\f}{\frac}
\newcommand{\p}{\partial}
\newcommand{\na}{\nabla}
%\newcommand{\Tr}{{\rm Tr}}
\newcommand{\tr}{{\rm tr}}
\newcommand{\STr}{{\rm STr}}
\newcommand{\la}{\langle}
\newcommand{\ra}{\rangle}
\newcommand{\bfa}{\mathbf{a}}
\newcommand{\bfb}{\mathbf{b}}
\newcommand{\bfc}{\mathbf{c}}
\newcommand{\bfd}{\mathbf{d}}
\newcommand{\bfe}{\mathbf{e}}
\newcommand{\bff}{\mathbf{f}}
\newcommand{\bfm}{\mathbf{m}}
\newcommand{\bfn}{\mathbf{n}}


\let\a=\alpha \let\b=\beta  \let\g=\gamma  \let\d=\delta
\let\z=\zeta  \let\h=\eta   \let\th=\theta \let\vth=\vartheta \let\k=\kappa \let\l=\lambda
\let\m=\mu    \let\n=\nu    \let\x=\xi      \let\r=\rho \let\om=\omega
\let\s=\sigma \let\t=\tau   \let\vph=\varphi
  \let\y=\upsilon  \let\si=\varsigma
\let\D=\Delta  \let\Th=\Theta \let\L=\Lambda \let\Om=\Omega

\let\vph=\varphi
\let\vphi=\varphi
\let\d=\delta
\let\G=\Gamma 
\newcommand{\uG}{\underline{G}}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


\DeclareMathOperator{\Tr}{Tr}
\DeclareMathOperator{\Det}{Det}

\newtheorem{definition}{Definition}[chapter]
\newtheorem{proposition}{Proposition}[chapter]
\newtheorem{lemma}{Lemma}[chapter]
\newtheorem{construction}{Construction}[chapter]
\newtheorem{theorem}{Theorem}[chapter]
\newtheorem{conjecture}{Conjecture}[chapter]
\newtheorem{corollary}{Corollary}[chapter]
\newtheorem{axiom}{Axiom}[chapter]

%\theoremstyle{definition}
\newtheorem{remark}{Remark}[chapter]
\newtheorem{example}{Example}[chapter]
\newtheorem{exercise}{Exercise}[chapter]

\newtheorem{question}{Question}
\newtheorem{answer}{Answer}

\renewcommand{\thefigure}{\arabic{chapter}.\arabic{figure}}

\renewcommand{\thefootnote}{\arabic{footnote}}

\renewcommand{\theequation}{\arabic{chapter}.\arabic{equation}}

\renewcommand{\thedefinition}{\arabic{chapter}.\arabic{definition}}

\renewcommand{\theproposition}{\arabic{chapter}.\arabic{proposition}}

\renewcommand{\thelemma}{\arabic{chapter}.\arabic{lemma}}

\renewcommand{\thetheorem}{\arabic{chapter}.\arabic{theorem}}

\renewcommand{\theconjecture}{\arabic{chapter}.\arabic{conjecture}}

\renewcommand{\theconstruction}{\arabic{chapter}.\arabic{construction}}

\renewcommand{\thecorollary}{\arabic{chapter}.\arabic{corollary}}

\renewcommand{\theremark}{\arabic{chapter}.\arabic{remark}}

\renewcommand{\theexample}{\arabic{chapter}.\arabic{example}}

\renewcommand{\theexercise}{\arabic{chapter}.\arabic{exercise}}

\definecolor{bluegray}{rgb}{0.4, 0.6, 0.8} 
\definecolor{brickred}{rgb}{0.8, 0.25, 0.33}
\definecolor{brightcerulean}{rgb}{0.11, 0.67, 0.84}
\definecolor{celestialblue}{rgb}{0.29, 0.59, 0.82}
\definecolor{darkpastelblue}{rgb}{0.47, 0.62, 0.8}
\definecolor{iceberg}{rgb}{0.44, 0.65, 0.82}
\definecolor{lightcornflowerblue}{rgb}{0.6, 0.81, 0.93}
\definecolor{lightskyblue}{rgb}{0.53, 0.81, 0.98}
\definecolor{palecornflowerblue}{rgb}{0.67, 0.8, 0.94}
\definecolor{britishracinggreen}{rgb}{0.0, 0.26, 0.15}
\definecolor{auburn}{rgb}{0.43, 0.21, 0.1}
\definecolor{bulgarianrose}{rgb}{0.28, 0.02, 0.03}
\definecolor{darkgreen}{rgb}{0.0, 0.2, 0.13}



\allowdisplaybreaks[4]

%\bibliographystyle{amsplain}

%\usepackage[backend=bibtex,bibstyle=trad-unsrt,doi=false,isbn=false,url=false,sorting=nyt]{biblatex}
%\usepackage[backend=bibtex,bibstyle=ieee,doi=false,isbn=false,url=false,sorting=nyt]{biblatex}
%\addbibresource{Refs.bib}

%\addbibresource{~/Desktop/lucru/Ongoing/Refs/Refs.bib}

\DeclareFieldFormat[article,inproceedings,book]{title}{\textit{#1}}
\DeclareFieldFormat[inproceedings]{booktitle}{{#1}}
\AtBeginBibliography{\renewcommand\finalandcomma{}}
\DeclareFieldFormat[article]{journaltitle}{\text{#1}}
%\DeclareFieldFormat[article]{volume}{\textbf{#1}}

%\DeclareFieldFormat[article]{pages}{ \text{#1}}
%\DeclareFieldFormat[article]{number}{}
%\DeclareFieldFormat[book]{volume}{}


\vbadness=9999
\tolerance=9999
\clubpenalty=10000
\widowpenalty=10000


\newlength{\drop} 

\newcommand*{\titleM}{\begingroup 
\drop = 0.08\textheight
\centering
\vspace*{\drop}
{\Huge\bfseries H\"ohere Mathematik}\par
\vspace*{2\drop}
{\Large\scshape R\u azvan Gheorghe Gur\u au}\par
\vspace*{2\drop}
{\scshape 

Institut f\" ur Theoretische Physik der Universit\" at Heidelberg, 
\\
Philosophenweg 19, 69120 Heidelberg, Germany 
}
\par
\vfill

\endgroup}
 

\makeatletter
\def\blfootnote{\xdef\@thefnmark{}\@footnotetext}
\makeatother

\begin{document}

%\thispagestyle{empty}

%\titleM

 
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%\newpage


%\thispagestyle{empty}

%${}$

%\newpage

\renewcommand{\thepage}{\roman{page}}

\setcounter{page}{1}

\thispagestyle{empty}

\titleM

%\dedicatie


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\cleardoublepage

\tableofcontents


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\cleardoublepage

\renewcommand{\thepage}{\arabic{page}}

\setcounter{page}{1}

%\part{H\"oMa I}

\chapter{Introduction}
 \emph{Axioms} are statements which are accepted to be true. 
 \emph{Theorems} (lemmatas, propositions, etc.) are statements that can be proven using logical reasoning starting from axioms. We know since the work of G\"odel that no system of axioms is complete, that is for any system of axioms which includes the natural numbers it is possible to formulate statements that are undecidable, that is can neither be proved true nor be proven false . This is because, essentially, there are more possible statements that can be formulated than there are possible proofs.
 
\emph{Reductio ad absurdum} is a strategy of proving a statement is true by first assuming the statement is false and proving that this implies a contradiction (i.e. some other false statement). As a true statement can not imply a false one, one concludes that the original statement is true. 

\emph{Mathematical induction} is a strategy of proving a statement indexed by a natural number $n$ is true by first proving it is true for $n=0$ and then proving that if the statement for $n$ is true then the one for $n+1$ is also true. Transfinite induction is indexed by ordinal numbers in stead of natural ones.

The following logic symbols are useful $\exists, !,\forall, \Rightarrow, \Leftrightarrow, =$. We denote $\equiv$ when the left hand side and the right hand side are equal by definition.

% {\color{red}Questions / plans
% \begin{itemize}
%  \item add chapter zero about logic?
%  \item add appendix about probability theory?
%  \item add appendix about holomorphic calculus, maybe focus on compact operators?
% \item add subsection with symplectic manifolds and Hamilton's equations in differential geometry?
% \end{itemize}
% }

\part{H\"oMa I}

\chapter{Sets and numbers}
 
\input{Preliminaries}
 
\chapter{Topological spaces}
  \label{ch:topo}

\input{TopoSpaces}

\chapter{Sequences}
\label{ch:sequences}

%\input{Sequences}
      
\chapter{Vector spaces, first contact}
\label{ch:FDVecspaces}
%\input{FDVecspaces}

\chapter{Matrices}

%\input{LinAl}


\chapter{Functions, first contact}
\label{ch:Rfunctions}

%\input{RFunctions}

\part{H\"oMa II}

\chapter{Spectral theory in finite dimensions}

%\input{Eigenvalues}

\chapter{Banach spaces}

\label{ch:vecBanach}
%\input{BVecspaces}
       
\chapter{Functions}
\label{ch:functions}

%\input{Functions}

 \chapter{The Riemann integral}
 \label{ch:integral}

%\input{SmoothInt}

\chapter{Elements of differential geometry}

% \input{DiffGeom}

\chapter{The Stokes theorem}

%\input{Stokes}

 \part{H\"oMa III}
   
 \chapter{Complex analysis}
  
% \input{ComplexAnalysis}

\chapter{Hilbert spaces \texttt{(Hilbert Raum)}} 
 \label{ch:HVecspaces}
 
%  \input{HVecspaces}
 
\chapter{The Lebesgue integral, first contact}
  \label{ch:Lebesgue}
 
% \input{Integration}
 
 \chapter{The Fourier transform}
 
%\input{FT}

 
 \chapter{Distributions}
   \label{ch:Distributions}
   
%\input{Distributions}

 
\chapter{Differential equations}
\label{ch:ODE}
%\input{ODE}


\appendix

\appendixpage
\noappendicestocpagenum
\addappheadtotoc

\chapter{Lie groups and representations, a primer}

%\input{MatrixGroups}

%\chapter{Elements of probability and statistics}

%\input{Proba}

%\chapter{Special functions}

%\input{Trigo}

\chapter{Exams}

%\input{Exams}



 
\cleardoublepage

\begingroup
\sloppy
\printbibliography[heading=bibintoc]
\endgroup


\end{document}
