---
layout: home
title: ""
---

# **Jinhua Wu**

I am a fourth-year PhD student in [SJTU-PLV](https://github.com/SJTU-PLV) at **[Shanghai Jiao Tong University](https://en.sjtu.edu.cn/)**. I am advised by Prof. [Yuting Wang](https://jhc.sjtu.edu.cn/~yutingwang/).

Email: \<first name>.\<last name>@sjtu.edu.cn

[GitHub](https://github.com/Hua-hana)

[Google Scholar](https://scholar.google.com/citations?user=FL33E5wAAAAJ&hl=en)

# **Research**

My current interests include verified compilation, Rust formalization and verification, and techniques for improving the usability of formal verification in critical systems such as operating systems.

I am currently working on a **verified Rust compiler** based on [CompCert](https://compcert.org/), which we call **RustCompCert**. Our goal is to formalize the most important compilation and checking passes in the official Rust compiler, including Drop Elaboration and Borrow Checking. The language we support is a safe, sequential subset. We exclude features such as polymorphism, traits, concurrency, and higher-order functions. Although unsafe code cannot be written directly in the language, we aim to support interoperability between safe and unsafe modules using techniques from [**verified compositional compilation**](https://dl.acm.org/doi/10.1145/3632914).

We have developed a workable prototype of RustCompCert, which we test extensively with a range of interesting cases, including borrow-checking examples (e.g., cases rejected by NLL but accepted by Polonius), safe Rust and C composition, and examples I collected from online discussions in the Rust community and from published papers.

I summarize the long-term roadmap of RustCompCert here, marking what has been finished and what has not:

- [x] A verified compiler for an ownership subset of Rust (i.e., Rust without reference), which serves as the framework of RustCompCert.
- [ ] Formalization and verification of the borrow checking algorithm:
  + [x] Implement the borrow checker based on Polonius
  + [ ] Verify the borrow checker (I already have an idea of how to prove it and am currently working on it)
- [ ] Support realistic Rust code. For example, using tools like [Charon](https://github.com/AeneasVerif/charon) to translate real Rust code to our language subset.
- [ ] Connect our verified compiler to some Rust verification tools to achieve end-to-end program verification.

# **Publications**

## Published

- Ling Zhang, Yuting Wang*, **Jinhua Wu**, Jérémie Koenig, and Zhong Shao. Fully Composable and Adequate Verified Compilation with Direct Refinements between Open Modules. Proceedings of the ACM on Programming Languages, 8(POPL), 2024.
  [[DOI](https://doi.org/10.1145/3632914) | [PDF](https://jhc.sjtu.edu.cn/~yutingwang/files/papers/popl24.pdf) | [Slides](https://jhc.sjtu.edu.cn/~yutingwang/files/slides/2024-popl.pdf) | [Code](https://github.com/SJTU-PLV/direct-refinement-popl24-artifact)]

- **Jinhua Wu**, Yuting Wang*, Meng Sun, Xiangzhe Xu, and Yichen Song. Towards a Framework for Developing Verified Assemblers for the ELF Format. The 21st Asian Symposium on Programming Languages and Systems (APLAS), 2023. 
  [[DOI](https://doi.org/10.1007/978-981-99-8311-7_10) | [Slides](https://jhc.sjtu.edu.cn/~yutingwang/files/slides/2023-aplas.pptx) | [Artifact](https://doi.org/10.5281/zenodo.8363543)]

- Xiangzhe Xu, **Jinhua Wu**, Yuting Wang*, Zhenguo Yin, and Pengfei Li. Automatic Generation and Validation of Instruction Encoders and Decoders. The 33rd International Conference on Computer-Aided Verification (CAV), 2021. 
  [[DOI](https://doi.org/10.1007/978-3-030-81688-9_34) | [Slides](https://jhc.sjtu.edu.cn/~yutingwang/files/slides/2021-cav-25mins.pptx) | [Artifact](https://zenodo.org/record/4720184#.YNBOZGgzZPY)]

## Preprint

- **Jinhua Wu**, Yuting Wang, Liukun Yu, Linglong Meng. End-to-end Compositional Verification of Program Safety through Verified and Verifying Compilation. [URL](https://arxiv.org/abs/2510.10015)

- **Jinhua Wu**, Yuting Wang, Liukun Yu, Linglong Meng. RustCompCert: A Verified and Verifying Compiler for a Sequential Subset of Rust. [URL](https://arxiv.org/abs/2602.07455)


<!-- # **Teaching Experience**

- **Teaching Assistant** for *Course Name*, term, by **Instructor Name**  
  - Add one line describing what you taught or supported.

- **Mentor / Tutor / Workshop Instructor** for *Program Name*, term  
  - Add one line describing the scope of the work.

- **Other Teaching**  
  - Add lectures, office hours, curriculum design, grading, lab support, or student mentoring. -->
