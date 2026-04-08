---
layout: post
title: physics as computation
date: 2026-04-08T 10:30:43-04:00
description: How light, heat, chemistry, and noise are replacing transistors as the fundamental substrate of intelligence — a critical survey of six paradigms reshaping the field.
categories: [physics, computation]
tags: [physics, computation, theory]
giscus_comments: true
related_posts: false
related_publications: false
---

> How light, heat, chemistry, and noise are replacing transistors as the fundamental substrate of intelligence — a critical survey of six paradigms reshaping the field.

For seven decades, computing has meant silicon. Transistors etched into crystalline wafers, toggling between 0 and 1 at ever-smaller scales, ever-faster clock speeds; a paradigm so dominant that most people have never imagined an alternative. But the physics of miniaturization is running out of runway. Heat walls, quantum tunneling at nanometer scales, and the staggering energy appetite of modern AI are forcing researchers to ask a more radical question: what if the computer *was* the physics, rather than fighting it?

In 2026, that question has produced a Cambrian explosion of unconventional computing paradigms. Researchers are not merely tweaking chip architectures; they are rethinking what computation *is*, drawing on thermodynamics, optics, molecular biology, and neuroscience. This article surveys six of the most active and scientifically credible areas, explains the core ideas with precision, and flags where bold claims deserve scrutiny.

---

## 01 — Thermodynamic Computing
### Harnessing the Noise: *Physics-Powered AI Acceleration*

`🔥 Hottest in 2026` `Hardware shipping` `Probabilistic AI` `Energy efficiency`

Every conventional computer is engaged in a perpetual war against its own physics. Transistors must operate thousands of times above the thermal noise floor to produce reliable binary outputs, a design philosophy that guarantees enormous energy waste. Thermodynamic computing takes the opposite stance: **embrace the noise, and use it as fuel.**

> **Key Concept:** The core principle: if a physical device operates at energy scales comparable to thermal energy ($k_B\  T$), it will spontaneously fluctuate between states. By carefully engineering the interactions between components, you can program these fluctuations to *solve problems*و the system "relaxes" toward its lowest-energy configuration, and that configuration is the answer.

The hardware manifestation is the **Stochastic Processing Unit (SPU)**, pioneered by Normal Computing. Their prototypeو eight RLC circuits (resistors, inductors, capacitors) coupled via switched capacitances on a printed circuit board  has already demonstrated Gaussian sampling and matrix inversion. A 2025 paper in *Nature Communications* showed it performing thermodynamic linear algebra, tasks that underpin generative AI and probabilistic modeling. Normal Computing has since announced the successful tape-out of **CN101**, described as the world's first thermodynamic computing chip designed for AI and HPC data centers.

A competing startup, **Extropic**, is pursuing a more ambitious vision: thermodynamic ASICs as a general-purpose acceleration layer sitting alongside CPUs and GPUs, routing computations to whichever physical substrate best matches the problem's structure.

> *"Classical and quantum computing fight noise. Thermodynamic computing is powered by it."*
> — Stephen Whitelam, Lawrence Berkeley National Laboratory, 2026

Berkeley Lab researchers published a framework in early 2026 for training thermodynamic neural networks — historically done expensively in simulation — and running inference on the physical hardware at drastically reduced energy cost. The current challenge is speed: these devices compute at equilibrium, which requires waiting for the system to settle. New work on non-equilibrium thermodynamic computing and Mpemba-effect-inspired initializations (using a "warm start" to accelerate convergence) is actively addressing this bottleneck.

A nuance worth stating clearly: thermodynamic computing overlaps substantially with probabilistic computing. The distinction is partly semantic — both leverage stochasticity — but thermodynamic computing grounds itself in the specific physical mechanisms of thermal fluctuations and energy landscapes from statistical mechanics, rather than purely algorithmic randomness.

**Key players:** Normal Computing · Extropic · Berkeley Lab / NERSC · Santa Fe Institute

**References:**
- Melanson et al. (2025). "Thermodynamic computing system for AI applications." *Nature Communications*, 16, 3757. [→ nature.com](https://www.nature.com/articles/s41467-025-59011-x)
- Whitelam, S. (2026). Berkeley Lab News: "Thermodynamic Computing Advances with Design and Training." [→ lbl.gov](https://newscenter.lbl.gov/2026/03/05/thermodynamic-computing-advances-with-design-and-training/)
- IEEE Spectrum (Aug 2025). "Thermodynamic Computing Is the Hot New Trend." [→ spectrum.ieee.org](https://spectrum.ieee.org/thermodynamic-computing-normal-computing)

---

## 02 — Neuromorphic Computing
### Spiking Silicon — *Brain-Inspired Processing at the Edge*

`Commercial 2026` `Robotics` `Edge AI` `Ultra-low power`

The human brain performs extraordinary feats of perception and coordination on roughly 20 watts — less than a dim light bulb. The secret is **sparsity**: biological neurons only fire when something changes, and they integrate memory directly with processing, eliminating the costly data shuttling that defines conventional von Neumann architectures.

Neuromorphic chips replicate this by implementing **Spiking Neural Networks (SNNs)** in silicon. Unlike the matrix multiplications of standard deep learning, SNNs process information as discrete events ("spikes") in time — consuming energy only when a signal actually occurs. Intel's **Loihi 3**, released in January 2026 on a 4nm process, packs 8 million neurons and 64 billion synapses per chip — an eightfold density increase over its predecessor — and introduces 32-bit "graded spikes" that bridge the gap between SNNs and traditional deep neural networks.

> ⚠ **Editorial Note:** IBM's **NorthPole**, while often grouped with neuromorphic chips, is more precisely a *near-memory inference accelerator*. It eliminates the von Neumann bottleneck by co-locating memory and compute, achieving up to 25× the energy efficiency of an H100 GPU for image recognition — but it does not use spiking neural networks. It is a complementary, not identical, paradigm. The original source text conflated these two distinct architectures.

Real-world deployments in 2026 include the ANYmal D Neuro quadruped robot, which runs on Loihi 3 for 72 continuous hours on a single charge — a ninefold improvement over GPU-powered predecessors. Mercedes-Benz and BMW are integrating neuromorphic vision for sub-millisecond autonomous braking reaction. Sandia National Laboratories has fielded the world's largest neuromorphic system (175 million neurons) for physics simulations previously requiring full supercomputers.

The remaining friction is software. Developers must "think in spikes" rather than tensors, and the tooling ecosystem — while improving with Intel's Lava framework — still lags the mature GPU stack. This remains the principal barrier to mainstream adoption.

**Key players:** Intel (Loihi 3) · IBM (NorthPole) · BrainChip (Akida 2.0) · SpiNNcloud

**References:**
- [Intel Labs Neuromorphic Research](https://www.intel.com/content/www/us/en/research/neuromorphic-computing.html)
- [IBM Research NorthPole](https://research.ibm.com/blog/northpole-ibm-ai-chip)

---

## 03 — Reversible Computing
### Never Erase a Bit — *Landauer's Principle and the Energy Floor*

`Thermodynamics` `Early stage` `AI training`

In 1961, IBM physicist Rolf Landauer established a profound result now bearing his name: **erasing information is physically irreversible and necessarily dissipates energy as heat**. Every time a transistor resets a bit, a minimum energy of k_B T·ln(2) must be released into the environment — a fundamental thermodynamic cost, not merely an engineering inefficiency.

> **Key Concept:** Reversible computing circumvents Landauer's limit by performing logic operations that are mathematically invertible. If you can always reconstruct the input from the output, you never truly "erase" information, and in principle you can reclaim the computational energy. The laws of physics permit it. The engineering challenge is formidable.

UK startup **Vaire Computing** is the leading commercial effort, building what they call "reversible silicon" — CMOS implementations of reversible logic gates designed to run large AI inference workloads at dramatically reduced heat output. The challenge is that reversible circuits require storing intermediate states (to allow reconstruction), which increases memory overhead. Making this practical at scale is an unsolved engineering problem, though Vaire's approach targets a pragmatic middle ground rather than theoretical perfection.

It's worth being precise: current reversible computing prototypes are not yet "near-zero heat waste" in practice. They demonstrate the principle and show meaningful efficiency gains in specific workloads. Claims of reclaiming energy should be understood as a theoretical ceiling, not a current product specification.

**Key players:** Vaire Computing · MIT CSAIL

**References:**
- Landauer, R. (1961). "Irreversibility and Heat Generation in the Computing Process." *IBM Journal of Research and Development.*
- ACM: [The Future is Reversible](https://queue.acm.org/detail.cfm?id=3588263) | [Vaire Computing](https://vaire.co)

---

## 04 — DNA & Molecular Computing
### Chemistry as Logic — *Biological Molecules as Computational Substrate*

`Massively parallel` `Long time horizon` `Data storage` `Wetware`

DNA is an almost absurdly efficient information storage medium. A single gram can theoretically hold around 215 petabytes of data — a figure derived from the information density of the four-nucleotide alphabet (A, T, G, C) and the physical scale of DNA molecules. (This is a theoretical maximum established in research published around 2016; practical read/write systems are currently orders of magnitude less efficient, but the trajectory is improving rapidly.)

DNA *computing* goes further than storage. In a test tube, billions of DNA strands can undergo hybridization — the process by which complementary sequences bind together — simultaneously. Each binding event can encode a logical operation. In 1994, Leonard Adleman demonstrated that DNA hybridization could solve an instance of the Hamiltonian path problem (a notoriously hard graph problem) in a test tube, performing billions of parallel computations without any electronic hardware.

> **Why It Matters for AI:** The primary appeal is massive parallelism at molecular scale and the convergence with synthetic biology. "Wetware" processing — where biological molecules both store and compute — could enable biosensors, drug discovery, and in-vivo diagnostics that current silicon cannot approach. The DNA32 Conference (August 2026, organized under ISNSCE) is the leading annual gathering of this community.

The limitations are real: DNA computing is slow by electronic standards (reactions take minutes to hours), error-prone, and programming it remains extremely difficult. It is best understood as a paradigm for specific problem classes — search, optimization, pattern matching — rather than a general-purpose replacement for CPUs.

**Key players:** Caltech Molecular Programming Project · Microsoft Research (DNA Storage) · Twist Bioscience

**References:**
- Adleman, L. (1994). "Molecular Computation of Solutions to Combinatorial Problems." *Science.*
- [Molecular Programming Project](https://molecularprogramming.org) | [DNA32 Conference](https://dna32.org)

---

## 05 — Optical (Photonic) Computing
### Computing with Light — *Photons for AI Matrix Arithmetic*

`AI hardware` `Venture-backed` `Bandwidth` `Low latency`

The central bottleneck of modern AI is matrix multiplication — the mathematical operation underlying virtually every neural network layer. On conventional hardware, this requires enormous numbers of multiply-accumulate operations, each burning energy as electrons flow through resistance. Photonic computing performs the same operation using light, where the physics are fundamentally different.

> **Key Concept:** Photons interact with optical components (beam splitters, phase shifters, modulators) to perform weighted summations — the core of matrix-vector multiplication — with *no resistive heat loss*. Multiple wavelengths (colors) of light can travel through the same waveguide simultaneously without interfering, enabling massive bandwidth in a single physical channel.

> ⚠ **Editorial Note:** A common overclaim: photonic computing is often described as operating "at the speed of light," implying an absolute speed advantage over electronics. This is misleading. Propagation delay is rarely the bottleneck in computing — the real advantages of photonics are **bandwidth density**, **absence of resistive heat**, and **natural parallelism via wavelength multiplexing**. The original source text repeated this common misconception.

**Lightmatter** is the leading player in photonic AI accelerators, building optical interconnects and matrix engines aimed at the next generation of AI training and inference clusters. Their architecture uses silicon photonics — photonic components fabricated using standard semiconductor processes — to make the technology manufacturable at scale.

> ⚠ **Editorial Note:** **Luminous Computing**, cited in the original source text, ceased operations in 2023. It should not be listed as an active player in this space. Lightmatter remains the primary commercial leader in photonic AI compute.

**Key players:** Lightmatter · Ayar Labs · PsiQuantum (hybrid)

**References:**
- [Lightmatter](https://lightmatter.co)
- Photonics100 2026 Innovation List (Photonics Media)

---

## 06 — Reservoir Computing (In-Materio)
### The World as a Computer — *Harnessing Physical Dynamics for Temporal Processing*

`Time-series` `Niche applications` `Physical AI`

Reservoir computing is perhaps the most conceptually surprising paradigm on this list. The idea, developed independently by Wolfgang Maass (liquid state machines) and Herbert Jaeger (echo state networks) around 2001, is that *any* sufficiently complex physical system with short-term memory can serve as a computational substrate — without being designed or trained in the conventional sense.

The process: encode an input signal into a physical system (a body of water, a network of carbon nanotubes, a mechanical metamaterial, an optical cavity). The system evolves according to its natural dynamics, creating a high-dimensional response. A simple linear readout layer is trained to extract the desired output from this response. The physics does the hard work of transforming the signal into a rich feature space.

> **In-Materio Computing:** A related thread — "in-materio" computing — uses disordered physical materials (nanowire networks, spintronic materials) as the computational substrate. The material itself is tuned by electrical signals until it solves a desired function. This dissolves the boundary between hardware and algorithm in a genuinely radical way.

Reservoir computing excels at **time-series tasks**: speech recognition, chaotic system prediction, financial time-series, weather sensing. It is extraordinarily energy-efficient because the "reservoir" consumes no training energy — only the thin readout layer is learned. The limitation is narrow applicability: it is not a general-purpose computing paradigm, and the engineering challenge of interfacing physical reservoirs with digital systems remains substantial.

**Key players:** Nantes University (photonic reservoirs) · Ghent University · NIST (nanowire reservoirs)

**References:**
- Maass, W. et al. (2002). "Real-time computing without stable states." *Neural Computation.*
- Tanaka, G. et al. (2019). "Recent advances in physical reservoir computing." *Neural Networks*, 115.
- npj Unconventional Computing (2025–26 issues). [→ nature.com/npjunconvcomput](https://www.nature.com/npjunconvcomput)

---

## Synthesis — Not One Winner: A Hardware Ecosystem
### *The Heterogeneous Future*

The most important thing to understand about Physics-as-Computation is that it is not a horse race with a single winner. Each paradigm is *fit to a problem class*: thermodynamic computers for probabilistic AI; neuromorphic chips for real-time sensory processing at the edge; photonic engines for matrix-intensive deep learning inference; DNA systems for massively parallel combinatorial search; reversible circuits for long-running, heat-constrained inference; reservoir systems for streaming time-series.

Normal Computing has articulated what may become the defining architectural vision for the coming decade: a heterogeneous computing stack where every computation is dispatched to a physical substrate whose natural dynamics most efficiently solve that particular class of problem. The CPU and GPU don't disappear — they become one chip type among many in a diverse ecosystem.

> **The Unifying Thread:** All six paradigms share a single intellectual ancestor: the recognition that conventional computing forces physics to do something unnatural — suppress, fight, and waste the very properties of the physical world. The post-silicon revolution is, at its core, a reconciliation between computation and physics. When you stop fighting the universe, it turns out the universe computes quite well on its own.

The field is young, claims are often premature, and the path from proof-of-concept to production silicon is littered with failed startups (Luminous being a cautionary example). But the scientific foundations — grounded in thermodynamics, quantum mechanics, and information theory — are sound. The research landscape of 2026 is not hype. It is a genuine paradigm transition, playing out in real time.


*PHYSICS AS COMPUTATION · RESEARCH SURVEY · APRIL 2026*
*For research and educational purposes. Based on my findings from the literature and recent sources.*
*Work in progress. Will post updates as my understanding of the field evolves.*





This theme implements a built-in Jekyll feature, the use of Rouge, for syntax highlighting.
It supports more than 100 languages.
This example is in C++.
All you have to do is wrap your code in markdown code tags:

````markdown
```c++
code code code
```
````

```c++
int main(int argc, char const \*argv[])
{
    string myString;

    cout << "input a string: ";
    getline(cin, myString);
    int length = myString.length();

    char charArray = new char * [length];

    charArray = myString;
    for(int i = 0; i < length; ++i){
        cout << charArray[i] << " ";
    }

    return 0;
}
```

For displaying code in a list item, you have to be aware of the indentation, as stated in [this FAQ](https://github.com/planetjekyll/quickrefs/blob/master/FAQ.md#q-how-can-i-get-backtick-fenced-code-blocks-eg--working-inside-lists-with-kramdown). You must indent your code by **(3 \* bullet_indent_level)** spaces. This is because kramdown (the markdown engine used by Jekyll) indentation for the code block in lists is determined by the column number of the first non-space character after the list item marker. For example:

````markdown
1. We can put fenced code blocks inside nested bullets, too.
   1. Like this:

      ```c
      printf("Hello, World!");
      ```

   2. The key is to indent your fenced block in the same line as the first character of the line.
````

Which displays:

1. We can put fenced code blocks inside nested bullets, too.
   1. Like this:

      ```c
      printf("Hello, World!");
      ```

   2. The key is to indent your fenced block in the same line as the first character of the line.

By default, it does not display line numbers. If you want to display line numbers for every code block, you can set `kramdown.syntax_highlighter_opts.block.line_numbers` to true in your `_config.yml` file.

If you want to display line numbers for a specific code block, all you have to do is wrap your code in a liquid tag:

{% raw %}
{% highlight c++ linenos %} <br/> code code code <br/> {% endhighlight %}
{% endraw %}

The keyword `linenos` triggers display of line numbers.
Produces something like this:

{% highlight c++ linenos %}

int main(int argc, char const \*argv[])
{
string myString;

    cout << "input a string: ";
    getline(cin, myString);
    int length = myString.length();

    char charArray = new char * [length];

    charArray = myString;
    for(int i = 0; i < length; ++i){
        cout << charArray[i] << " ";
    }

    return 0;

}

{% endhighlight %}

