# EIHeader
A head file for C/C++ ELF extract/rebuild whose source file is missing.

## Functions can register now
* EIS_secfnd - call when found a section
* EIS_segfnd - call when found a segment
* EIS_relfnd - call when found a relocation

## Usage
elf_rinit - call before use

elf_mark - load the elf info

Transformers:

a-address after load to memory; o-offset in elf; p-pointer in this code context

static byte_t*  elf_a2p(ptr_t p_addr);

static byte_t*  elf_o2p(dword_t p_ofst);

static dword_t  elf_a2o(ptr_t p_addr);

static dword_t  elf_p2o(byte_t* p_ptr);

static ptr_t    elf_o2a(dword_t p_ofst);

static ptr_t    elf_p2a(byte_t* p_ptr);
