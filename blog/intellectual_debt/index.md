---
layout: page
title: Short note of the talk "Intellectual Debt and the Death of the Programmer" by Professor Neil D. Lawrence
tags: []
modified:
comments: true
---
<p>This is a short note of the talk "Intellectual Debt and the Death of the Programmer" by Professor Neil D. Lawrence which can be found <a href="http://inverseprobability.com/talks/notes/intellectual-debt-and-the-death-of-the-programmer.html">here</a></p>

<h2>Intellectual Debt and the Death of the Programmer</h2>

<ul>
  <li>Problem : Intellectual debt in AI/ML systems
    <ul>
      <li>Technical debt is the inability to maintain your complex software system. It is incurred when complex systems are rapidly deployed without due thought as to how they will be maintained.</li>
      <li>Intellectual debt is the inability to explain your software system. It is incurred when complex systems are rapidly deployed without due thought to how they’ll be explained. </li>
    </ul>
  </li>
  <li>Causes ? : Rapid deployment, Complex systems desing approaches and The Great AI Fallacy
    <ul>
      <li>Lean Startup Methodology : Using the least effort required to get your machine learning model deployed. The idea is that you should build the quickest thing possible to test your market and see if your idea works. Only when you know your idea is working should you invest more time and personnel in the software.</li>
      <li>There is a tension between deploying quickly and deploying a maintainable system.</li>
      <li>The Great AI Fallacy : AI will adapt to the human. This is causing us to suspend our calibrated skepticism that is needed to deploy these systems safely and efficiently.</li>
      <li>"separation of concerns" approach to desing complex systems: The idea is that you architect your system, which consists of a large-scale complex task, into a set of simpler tasks. Each of these tasks is separately implemented. But this means no one is concerned about the overall system itself.</li>
    </ul>
  </li>
  <li>Complex Systems:
    <ul>
      <li>It is difficult for a single individual to understand and there is no physical manifestation of the system to inspect.</li>
      <li>Adding data to complex systems make things much worse.</li>
    </ul>
  </li>
  <li>Service-oriented Architecture:
    <ul>
      <li>This is the general approach to large scale software infrastructure.</li>
      <li>Ownership of each component in the system is assigned to a small team. They design, build and maintain it in production.</li>
    </ul>
  </li>
  <li>“The Death of the Programmer” occurs in the service-oriented architecture framework, because whatever the intent of the team that built and maintains each individual service, once it is deployed the service can be consumed for whichever purpose. It is beyond the control of the original programmers.</li>
  <li>The long-term challenge is not in the interpretability of individual models. The long-term challenge is the complex interaction between different components in the decomposed system, where the original intent of each component has been forgotten and each service has been repurposed.</li>
  <li>What would be a possible solution? author suggests that we should move from FIT Models to FIT Systems.
    <ul>
      <li>FIT: fair, interpretable and transparent</li>
    </ul>
  </li>
  <li>Proposed roadmap for solution contains broadly two parts.
  <ol>
    <li>“Data-Oriented Architectures”
      <ul>
        <li>Aims to address the complexity in current interaction between the services in a service-oriented architecture by introducing data-oriented programming.</li>
        <li>Data-oriented programming is not only about the individual services, but how they are connected.</li>
        <li>If each service has its inputs and outputs declared on a wider ecosystem, then we can programmatically determine which inputs effect which decisions.</li>
      </ul>
    </li>
    <li>“meta modelling”, machine learning techniques that help us model the models.</li>
  </ol>
  </li>
  <li>Conclusion:
    <ul>
      <li>The author suggests that the way we doing AI/ML will lead us to a point where we will be unable to explain the complex decisions being made by ML systems.</li>
      <li>Author proposes a roadmap that consisits the notions of "data-oriented architectures" and "meta modelling"</li>
    </ul> 
   </li>
</ul>

