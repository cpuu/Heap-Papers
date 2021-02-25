# Heap-Papers

## Heap Exploitation Techniques

| Name | Description | Reference |
|---|:---|---:|
|`Fast bin dup` | Corrupting a fast bin freelist (e.g., by double free or write-after-free) to return an arbitrary location |---:|
|  `Unsafe unlink` | Abusing unlinking in a freelist to get arbitrary write |---:|
| `House of spirit` | Freeing a fake chunk of fast bin to return arbitrary location |---:|
| `Poison null byte` |  Corrupting heap chunk size to consolidate chunks even in the presence of allocated heap |---:|
| `House of lore` | Abusing the small bin freelist to return an arbitrary location |---:|
| `Overlapping chunks` |  Corrupting a chunk size in the unsorted bin to overlap with an allocated heap |---:|
| `House of force` |  Corrupting the top chunk to return an arbitrary location |---:|
| `Unsorted bin attack` | Corrupting a freed chunk in unsorted bin to write a uncontrollable value to arbitrary location  |---:|
|`House of einherja` |Corrupting PREV_IN_USE to consolidate chunks to return an arbitrary location that requires a heap address |[14]|
|`Unsorted bin into stack` |  Abusing the unsorted freelist to return an arbitrary location |[16]|
|`House of unsorted einherjar` | A variant of house of einherjar that does not require a heap address  |[16]|
|`Unaligned double free` | Corrupting a small bin freelist to return already allocated heap  |[16]|
|`Overlapping small chunks` |  Corrupting a chunk size in a small bin to overlap chunks |[16]|
|`Fast bin into other bin` | Corrupting a fast bin freelist and use malloc_consolidate() to return an arbitrary non-fast-bin chunk |[16]|


## Secure Heap Allocator Design
- Berger, Emery D., and Benjamin G. Zorn. `"DieHard: Probabilistic memory safety for unsafe languages."` Acm sigplan notices 41.6 (2006): 158-168.
- Novark, Gene, and Emery D. Berger. `"DieHarder: securing the heap."` Proceedings of the 17th ACM conference on Computer and communications security. 2010.

## Reading
| # | Year | Title | Review |
|---|:---:|:---|---:|
| 1 | 2001 | [Vudo malloc tricks](http://phrack.org/issues/57/8.html) |  |
| 2 | 2001 | [Once upon a free()...](http://phrack.org/issues/57/9.html) |  |
| 3 | 2003 | [Advanced Doug lea’s malloc exploits](http://phrack.org/issues/61/6.html) |  |
| 4 | 2004 | [Exploiting the wilderness](https://seclists.org/vuln-dev/2004/Feb/25) |  |
| 5 | 2007 | [The use of set_head to defeat the wilderness](http://phrack.org/issues/64/9.html) |  |
| 6 | 2007 | [Understanding the heap by breaking it](https://www.exploit-db.com/download/17249) |  |
| 7 | 2009 | [Yet another free() exploitation technique](http://phrack.org/issues/66/6.html) |  |
| 8 | 2009 | [Malloc Des-Maleficarum](http://phrack.org/issues/) |  |
| 9 | 2010 |  [The house of lore: Reloaded](http://phrack.org/issues/67/8.html) |  |
| 10 | 2014 | [The poisoned NUL byte, 2014 edition](https://googleprojectzero.blogspot.com/2014/08/the-poisoned-nul-byte-2014-edition.html) |  |
| 11 | 2015 |[Glibc adventures: The forgotten chunk](https://www.contextis.com/en/resources/white-papers/glibc-adventures-the-forgotten-chunks) |  |
| 12 | 2016 | [Ptmalloc fanzine](http://tukan.farm/2016/07/26/ptmalloc-fanzine/) |  |
| 13 | 2016 | [New exploit methods against Ptmalloc of Glibc](https://loccs.sjtu.edu.cn/~romangol/publications/trustcom16.pdf)|  |
| 14 | 2016 | [House of Einherjar](https://github.com/st4g3r/House-of-Einherjar-CB2016) |  |
| 15 | 2018 | [HeapHopper](https://www.usenix.org/conference/usenixsecurity18/presentation/eckert) |  |
| 16 | 2020 | [ArcHeap](https://github.com/sslab-gatech/ArcHeap) |  |