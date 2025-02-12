---
layout: page
title: Developing an Agent
permalink: /agentdev/
---

All your code should be placed in a module called group$n$, i.e. a file called \textit{group$n$.py}, where $n$ is the group number that will be allocated to you.
The main agent class (being a subclass of TradingCompany) and implementing \texttt{pre\_inform}, \texttt{inform} and \texttt{receive} or related functions, as described in the getting started section, should be named Company$n$, where $n$ is again your group number.
For example, for group $5$, the resulting qualified name of the agent object becomes \texttt{group5.Company5}.

Further details on starting to develop an agent can be found in the getting started section and the \href{https://mable-doc.netlify.app/}{MABLE API}.

For the submission, agents need to be accompanied by a report (see Section~\ref{sec:report}).
Please submit your agent and the report together in one zip file by the deadline.
