# PSD Ecosystem Documentation

This repository collects project, software, infrastructure, and licensing
documents related to the PSD Ecosystem. It currently consists primarily of
PDF publications, with a small number of editable ODT documents, a PPTX
presentation, and a plain-text proposal. The [Turkish README](<README.tr.md>)
is also available.
This edition uses American English with a light, conversational New York feel:
plainspoken and direct, never dressed up in forced slang.

## Document Library

### PSD Ecosystem and GNU/Linux

- [PSD Ecosystem, document 1](<ecosystem/PSD_Ecosystem.pdf>)
- [PSD Ecosystem, document 2](<ecosystem/PSD_Ecosystem2.pdf>)
- [PSD Ecosystem, document 3](<ecosystem/PSD_Ecosystem3.pdf>)
- [What Is PSD?](<ecosystem/psdnedir.pdf>)
- [Civilian PSD GNU/Linux Copyleft](<ecosystem/psdgnulinux_sivil_copyleft.pdf>)
- [Companies that modify the Linux kernel and why (Turkish)](<ecosystem/linux_kernel_modifikasyonlari.pdf>)

### User Interfaces and Development

- [PSD TUI](<interfaces/psdtui.pdf>) and [PSD TUI, document 2](<interfaces/psdtui2.pdf>)
- [C++ Kernel](<kernel/cppkernel.pdf>)
- [Kernel Programming 101](<kernel/kernel_programming_101.pdf>)
- [Framework-based AI versus OS-integrated AI (Turkish)](<kernel/work.pdf>)
- [Linux and GNU developers: forking the Linux kernel and licensing (Turkish)](<kernel/linuxgnudevelopers.pdf>)
- [Can I Write Userspace Drivers with C++ for Hurd?](<kernel/C++ Can I write userspace drivers with C++ for hurd.pdf>)
- [Hurd](<kernel/hurd.pdf>)
- [Linux and C++](<kernel/linuxcpp.pdf>)
- [Memory Management with C++](<kernel/memcpp.pdf>)
- [Linux kernel security learning roadmap: from kernel development to responsible research (Turkish)](<kernel/psdexploit.pdf>) ([editable ODT](<kernel/psdexploit.odt>))
- [Network Subsystem for Linux](<networking/network subsystem for linux.pdf>)
- [Federated text-based chat network architecture and IRC automation guide (English)](<networking/federated-irc-architecture-guide.pdf>)
- [Private Matrix and Element deployment guide (English)](<networking/matrix.pdf>): covers server isolation, client customization, LDAP and Active Directory integration, and multiplatform clients.
- [matrix-rust-sdk presentation (English)](<networking/matrix_rust_sdk_nyc_presentation.pptx>): a presentation on the SDK's architecture, encryption, async bot example, operations, and cross-platform use.
- [Unix Development](<unix/unixdev.pdf>) ([editable ODT](<unix/unixdev.odt>))

### Lisp and Shell Languages

- [QShell repository exploration guide (Turkish)](<lisp/bu depoda dikkat etmem gereken yerler nelerdir qsh.pdf>) ([Markdown](<lisp/bu depoda dikkat etmem gereken yerler nelerdir qsh.md>)): an overview of the Guile-based architecture and areas to examine when developing QShell for system scripting.

### Distribution Planning

- [PSD repository assessment and architecture outlook (Turkish)](<distributions/bu depoda dikkat etmem gereken yerler nelerdir qsh 1.pdf>) ([Markdown](<distributions/bu depoda dikkat etmem gereken yerler nelerdir qsh 1.md>)): an assessment of the repository as design documentation, the envisioned Kernel, UMFS, Guile, and QShell layering, and suggested priorities.
- [Git platform release workflows, APIs, and open-source status (Turkish)](<distributions/release_tools.pdf>): an overview of release processes on GitHub, GitLab, Forgejo, and Codeberg, the APIs used by CLI tools, platform licensing, and OpenAPI specifications.

### MassForge

- [Git and CI/CD platform architecture design (Turkish)](<massforge/git_platform_mimari_tasarimi.pdf>) ([Markdown](<massforge/git_platform_mimari_tasarimi.md>)): an architecture roadmap for a high-performance Git and CI/CD platform using C/C++ and GNU Assembler, covering the core, storage, CI/CD engine, web stack, and scaling.
- [Forgejo registration approval and administrator notification settings (Turkish)](<massforge/forgejo-kayit-onay-ayarlari.pdf>): a guide to configuring registration approval and email notifications, restarting Forgejo, and testing mail delivery.
- [Forgejo and Woodpecker CI infrastructure and budget plan (Turkish)](<massforge/forgejo_infrastructure.pdf>): a proposed multi-architecture build and hardware testing infrastructure, with hardware, data center capacity, and cost estimates.

### Community, Organizations, and Services

- [KamuNet](<networking/kamunet.pdf>)
- [DAO](<organizations/dao.pdf>) ([editable ODT](<organizations/dao.odt>))
- [QB Networks startup proposal](<organizations/qbnetworks_startup.pdf>) ([editable ODT](<organizations/qbnetworks_startup.odt>); [plain text](<organizations/qbnetworks_startup.txt>))
- [Serebral](<organizations/serebral.pdf>)
- [MassCollabs services](<organizations/mass.tr.pdf>)

### Licensing

- [Licensing 101](<licensing/lisanslama-101.pdf>) and [Licensing 101, document 2](<licensing/lisanslama-101-2.pdf>)
- [BSD 3-Clause and BNGPL comparison](<licensing/bsd3clause_vs_bngpl.pdf>)
- [Framework under BNGPL 1.0 or later](<licensing/framework_bngpl.pdf>)
- [Military BNGPL licensing](<licensing/askerilisans.pdf>)
- [BNGPL 1.0](<licensing/bngpl-1.0.md>), [BNGPL 2.0](<licensing/bngpl-2.0.md>), and [BNGPL 3.0](<licensing/bngpl-3.0.md>)
- [GNU Affero General Public License 3.0](<LICENSE>)
- [Creative Commons Attribution-ShareAlike 4.0](<by-sa.markdown>)

### File Systems

- [File system and Linux file system development guide (Turkish)](<filesystems/dosya_sistemi_rehberi.pdf>) ([Markdown](<filesystems/dosya_sistemi_rehberi.md>))
- [Disk security, file systems (ZFS and Ceph focus), and digital forensics guide (Turkish)](<filesystems/disk_ve_veri_guvenligi_rehberi.pdf>) ([Markdown](<filesystems/disk_ve_veri_guvenligi_rehberi.md>))
- [Debian PSD UMFS guide](<filesystems/debianpsdumfs.pdf>) ([Markdown](<filesystems/debianpsdumfs.md>))
- [UMFS theory (Turkish)](<filesystems/umfs/umfs_theory.pdf>) ([Markdown](<filesystems/umfs/umfs_theory.md>))
- [UMFS bindings (Turkish)](<filesystems/umfs/bu yapida bindings ne anlama gelir.pdf>) ([Markdown](<filesystems/umfs/bu yapida bindings ne anlama gelir.md>))
- [UMFS bindings, part 1: Guile (Turkish)](<filesystems/umfs/bu yapida bindings ne anlama gelir 1.pdf>) ([Markdown](<filesystems/umfs/bu yapida bindings ne anlama gelir 1.md>))
- [UMFS bindings, part 2: licensing (Turkish)](<filesystems/umfs/bu yapida bindings ne anlama gelir 2.pdf>) ([Markdown](<filesystems/umfs/bu yapida bindings ne anlama gelir 2.md>))
- [ext2/ext3 code analysis](<filesystems/ext2-3/ext2fs_kod_analizi.pdf>) ([Markdown](<filesystems/ext2-3/ext2fs_kod_analizi.md>))
- [Hurd file system guide](<filesystems/hurd/hurd_filesystem_guide.pdf>) ([Markdown](<filesystems/hurd/hurd_filesystem_guide.md>))
- [PSD file system guide](<filesystems/psdfs/psd_dosya_sistemi_kilavuzu.pdf>) ([Markdown](<filesystems/psdfs/psd_dosya_sistemi_kilavuzu.md>))
- [ReFS and Windows file systems report](<filesystems/windowsfs/refs_ve_windows_dosya_sistemleri_raporu.pdf>) ([Markdown](<filesystems/windowsfs/refs_ve_windows_dosya_sistemleri_raporu.md>))

### Society and Licensing Analysis

- [Comparison of AGPL and BNGPL from a Marxist perspective (Turkish)](<society/lisans_society.pdf>) ([Markdown](<society/lisans_society.md>))
- [Marxist comparison of AGPL and BNGPL licenses (Turkish)](<society/lisanslarin_marksist_karsilastirmasi.pdf>) ([Markdown](<society/lisanslarin_marksist_karsilastirmasi.md>))
- [Expanded Marxist comparison of AGPL and BNGPL licenses, version 2 (Turkish)](<society/lisanslarin_marksist_karsilastirmasi_v2.pdf>) ([Markdown](<society/lisanslarin_marksist_karsilastirmasi_v2.md>))
- [Marxist-Leninist/Socialist/Communist perspective and analysis of a business](society/merkez.pdf)
- [Decentralized AGPLv3-or-later focused business and organization model](society/merkeziyetsiz.pdf)

### Memory

- [Memory overview](<memory/bellek.pdf>)
- [Memory allocation, document 1](<memory/malloc_1.pdf>)
- [Memory allocation, document 2](<memory/malloc_2.pdf>)
- [What is a segmentation fault? (Turkish)](<memory/segmentation_fault_nedir.pdf>): an overview of common causes, memory protection, and debugging with GDB and Valgrind.

## Project History

The repository's development, from its first commit onward, is summarized
below:

- **October 7, 2026:** Started the collection with three PSD Ecosystem
  publications and added two PSD TUI publications.
- **October 8, 2026:** Added documents on C++ kernels, Hurd, C++ userspace
  drivers, Linux, memory management, Linux networking, and KamuNet.
- **October 9, 2026:** Added licensing guides, DAO publications, an
  introduction to PSD, and the QB Networks startup proposal. Established
  repository basics with `.gitignore`, `README.md`, and an initial MIT
  `LICENSE`.
- **October 10, 2026:** Added Unix development material and published BNGPL
  1.0, updating the root license and README.
- **October 11, 2026:** Added publications comparing BSD 3-Clause and BNGPL,
  presenting a BNGPL framework, documenting LibreOffice support for
  Serebral, and describing MassCollabs services.
- **October 12, 2026:** Published BNGPL 2.0 and 3.0 and updated the root
  license and README; added military BNGPL material and recorded an
  AGPLv3-or-later exception for the civilian PSD GNU/Linux copyleft
  publication.
- **October 18, 2026:** Added three memory publications.
- **October 18, 2026:** Added the AGPL 3.0 license text and documented the
  complete project history and license terms in this repository.
- **October 18, 2026:** Added the *Kernel Programming 101* publication.
- **October 18, 2026:** Added `work.pdf` on framework-based versus
  OS-integrated AI, and `linuxgnudevelopers.pdf` on forking the Linux kernel
  and its GPLv2, GPLv3, and AGPLv3 licensing implications.
- **October 24, 2026:** Added a file system documentation section under
  `filesystems/` covering ext2/ext3, Hurd, PSD, and ReFS/Windows file systems, each in
  Markdown and PDF formats.
- **October 25, 2026:** Added `society/`, a Turkish-language comparison of the
  AGPL and BNGPL licenses from a Marxist perspective, in Markdown and PDF
  formats.
- **October 25, 2026:** Added two more Turkish-language Marxist comparisons of
  the AGPL and BNGPL licenses under `society/`, including an expanded second
  version, in Markdown and PDF formats.
- **October 26, 2026:** Organized publications into topic folders while
  retaining the existing file-system and society documentation folders.
- **October 26, 2026:** Added `filesystems/umfs/umfs_theory`, a Turkish-language UMFS
  design discussion covering the kernel and system scripting layers and AI
  considerations, in Markdown and PDF formats.
- **October 26, 2026:** Added three Turkish-language UMFS notes under
  `filesystems/umfs/` on language bindings, embedding Guile as a Lisp engine, and
  AGPL v3 or later licensing, in Markdown and PDF formats.
- **October 26, 2026:** Added a Turkish-language QShell repository guide in
  Markdown and PDF formats, covering the Guile-based architecture, key
  directories, and system scripting considerations.
- **October 26, 2026:** Added a Turkish-language assessment of the repository
  and the envisioned Kernel, UMFS, Guile, and QShell architecture under
  `distributions/`, in Markdown and PDF formats.
- **October 28, 2026:** Added `massforge/`, a Turkish-language architecture
  design for a high-performance C/C++ and GNU Assembler Git and CI/CD
  platform, in Markdown and PDF formats.
- **October 31, 2026:** Added `filesystems/disk_ve_veri_guvenligi_rehberi`, a
  Turkish-language guide to disk security, file systems with a ZFS and Ceph
  focus, and digital forensics, in Markdown and PDF formats.
- **November 8, 2026:** Added `ecosystem/linux_kernel_modifikasyonlari.pdf`, a
  Turkish-language overview of the companies that modify the Linux kernel and
  their motivations, in PDF format.
- **November 10, 2026:** Added `kernel/psdexploit`, a Turkish-language Linux
  kernel security learning roadmap that favors kernel development, debugging,
  fuzzing, and responsible disclosure, in editable ODT and PDF formats.
- **November 11, 2026:** Added `networking/federated-irc-architecture-guide.pdf`,
  an English-language guide to federated text-based chat network architecture
  and IRC automation, in PDF format.
- **November 11, 2026:** Renamed `bellek/`, `distro/`, `fs/`, and `lısp/` to
  `memory/`, `distributions/`, `filesystems/`, and `lisp/`, respectively, and
  updated the README links. File names stayed the same.
- **November 12, 2026:** Added `distributions/release_tools.pdf`, a
  Turkish-language overview of Git platform release workflows, CLI APIs,
  licensing, and OpenAPI specifications.
- **November 12, 2026:** Added `massforge/forgejo-kayit-onay-ayarlari.pdf`,
  a Turkish-language guide to Forgejo registration approval and administrator
  email notifications.
- **November 12, 2026:** Added `memory/segmentation_fault_nedir.pdf`, a
  Turkish-language overview of segmentation faults, their causes, and
  debugging tools.
- **November 12, 2026:** Added `networking/matrix.pdf`, an English-language
  guide to private Matrix and Element deployment, authentication integration,
  server isolation, and client customization.
- **November 12, 2026:** Added `networking/matrix_rust_sdk_nyc_presentation.pptx`,
  an English-language presentation on matrix-rust-sdk architecture,
  encryption, an async bot example, and cross-platform use.
- **November 13, 2026:** Added `massforge/forgejo_infrastructure.pdf`, a
  Turkish-language Forgejo and Woodpecker CI infrastructure and budget
  planning report covering multi-architecture builds and hardware testing.
- **November 14, 2026:** Changed the program license from BNGPL 3.0-or-later
  to AGPL 3.0-or-later and set the documentation license to CC BY-SA 4.0 or
  later. Added the CC BY-SA 4.0 text, removed the separate AGPL text and
  former license exception file, and updated the README license notices.

The [ChangeLog](<ChangeLog>) records changes from the first commit through
the latest project commit and names the documents added at each stage.

## License

Copyright (c) 2026-2027 PSD Authors.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

## Documentation License

[CC BY-SA 4.0 or later](by-sa.markdown)
