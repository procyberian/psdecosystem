# PSD Ecosystem Documentation

This repository collects project, software, infrastructure, and licensing
documents related to the PSD Ecosystem. It currently consists primarily of
PDF publications, with a small number of editable ODT documents and a
plain-text proposal. The [Turkish README](<README.tr.md>) is also available.

## Document Library

### PSD Ecosystem and GNU/Linux

- [PSD Ecosystem, document 1](<ecosystem/PSD_Ecosystem.pdf>)
- [PSD Ecosystem, document 2](<ecosystem/PSD_Ecosystem2.pdf>)
- [PSD Ecosystem, document 3](<ecosystem/PSD_Ecosystem3.pdf>)
- [What Is PSD?](<ecosystem/psdnedir.pdf>)
- [Civilian PSD GNU/Linux Copyleft](<ecosystem/psdgnulinux_sivil_copyleft.pdf>)

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
- [Network Subsystem for Linux](<networking/network subsystem for linux.pdf>)
- [Unix Development](<unix/unixdev.pdf>) ([editable ODT](<unix/unixdev.odt>))

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
- [GNU Affero General Public License 3.0](<licensing/agpl-3.0.md>)
- [License exception](<licensing/exception.md>): the civilian PSD GNU/Linux copyleft document is identified as AGPLv3-or-later.

### File Systems

- [File system and Linux file system development guide (Turkish)](<fs/dosya_sistemi_rehberi.pdf>) ([Markdown](<fs/dosya_sistemi_rehberi.md>))
- [Debian PSD UMFS guide](<fs/debianpsdumfs.pdf>) ([Markdown](<fs/debianpsdumfs.md>))
- [UMFS theory (Turkish)](<fs/umfs/umfs_theory.pdf>) ([Markdown](<fs/umfs/umfs_theory.md>))
- [ext2/ext3 code analysis](<fs/ext2-3/ext2fs_kod_analizi.pdf>) ([Markdown](<fs/ext2-3/ext2fs_kod_analizi.md>))
- [Hurd file system guide](<fs/hurd/hurd_filesystem_guide.pdf>) ([Markdown](<fs/hurd/hurd_filesystem_guide.md>))
- [PSD file system guide](<fs/psdfs/psd_dosya_sistemi_kilavuzu.pdf>) ([Markdown](<fs/psdfs/psd_dosya_sistemi_kilavuzu.md>))
- [ReFS and Windows file systems report](<fs/windowsfs/refs_ve_windows_dosya_sistemleri_raporu.pdf>) ([Markdown](<fs/windowsfs/refs_ve_windows_dosya_sistemleri_raporu.md>))

### Society and Licensing Analysis

- [Comparison of AGPL and BNGPL from a Marxist perspective (Turkish)](<society/lisans_society.pdf>) ([Markdown](<society/lisans_society.md>))
- [Marxist comparison of AGPL and BNGPL licenses (Turkish)](<society/lisanslarin_marksist_karsilastirmasi.pdf>) ([Markdown](<society/lisanslarin_marksist_karsilastirmasi.md>))
- [Expanded Marxist comparison of AGPL and BNGPL licenses, version 2 (Turkish)](<society/lisanslarin_marksist_karsilastirmasi_v2.pdf>) ([Markdown](<society/lisanslarin_marksist_karsilastirmasi_v2.md>))

### Memory

- [Memory overview](<bellek/bellek.pdf>)
- [Memory allocation, document 1](<bellek/malloc_1.pdf>)
- [Memory allocation, document 2](<bellek/malloc_2.pdf>)

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
  `fs/` covering ext2/ext3, Hurd, PSD, and ReFS/Windows file systems, each in
  Markdown and PDF formats.
- **October 25, 2026:** Added `society/`, a Turkish-language comparison of the
  AGPL and BNGPL licenses from a Marxist perspective, in Markdown and PDF
  formats.
- **October 25, 2026:** Added two more Turkish-language Marxist comparisons of
  the AGPL and BNGPL licenses under `society/`, including an expanded second
  version, in Markdown and PDF formats.
- **October 26, 2026:** Organized publications into topic folders while
  retaining the existing file-system and society documentation folders.
- **October 26, 2026:** Added `fs/umfs/umfs_theory`, a Turkish-language UMFS
  design discussion covering the kernel and system scripting layers and AI
  considerations, in Markdown and PDF formats.

The [ChangeLog](<ChangeLog>) records changes from the first commit through
the latest project commit and names the documents added at each stage.

## License

Copyright (c) 2026-2027 PSD Authors.

Unless a document-specific exception applies, this repository is licensed
under the Broad Netwide General Public License (BNGPL), Version 3.0, or a
later version officially released by the Project Owner that permits that
upgrade path. See [LICENSE](<LICENSE>) and the [BNGPL 3.0 text](<licensing/bngpl-3.0.md>)
for the terms. The exception for
[psdgnulinux_sivil_copyleft.pdf](<ecosystem/psdgnulinux_sivil_copyleft.pdf>) is recorded
in [exception.md](<licensing/exception.md>).

This material is provided "as is," without warranty. If it is conveyed as a
binary or deployed through a cloud or SaaS interface, the applicable BNGPL
terms require access to the copyright and license notices as specified in
the license.
