---
title: 'ISO/IEC JTC1/SC22/WG14 document N3299 to ISO/IEC 9899:2024 (en) conversion'
author: Ian Abbott
date: 2025-07-03
---

# ISO/IEC JTC1/SC22/WG14 document N3299 to ISO/IEC 9899:2024 (en) conversion

## Introduction

Document [N3299](https://www.open-std.org/jtc1/sc22/wg14/www/docs/n3299.pdf) is
an early draft of the next version of the C standard (codename C2y). It is
broadly similar to the ISO/IEC 9899:2024 standard (codename C23 or C24).

This document describes how to change the text of N3299 to match ISO/IEC
9899:2024 (en).

## General

* The cover sheet containing the abstract has been replaced.

* The small, running paragraph numbers in the left margin of the draft standard
  are not present in the published standard.

## 3.6

* Remove the following from the end of paragraph 1:

    > It may not be possible to express the address of each individual bit of an
    > object.

* Add paragraph 2:

    > Note 1 to entry: It is possible that each individual bit of an object is
    > not addressable.

## 3.7

* Replace paragraph 2 with:

    > Note 1 to entry: Each individual byte of an object is uniquely
    > addressable.

## 3.

* Add sections 3.29 to 3.31:

    > ## 3.29
    > ### out-of-bounds store
    > (attempted) access (3.1) that, at run time, for a given computational
    > state, would modify (or, for an object declared **`volatile`**, fetch) one
    > or more bytes that lie outside the bounds permitted by this document.
    > 
    > ## 3.30
    > ### bounded undefined behavior
    > undefined behavior (3.5.3) that does not perform an out-of-bounds store.
    > 
    > Note 1 to entry: The behavior can perform a trap.
    > 
    > Note 2 to entry: Any values produced can be unspecified values, and the
    > representation of objects that are written to can become indeterminate.
    >
    > ## 3.31
    > ### critical undefined behavior
    > undefined behavior that is not bounded undefined behavior.
    > 
    > Note 1 to entry: The behavior can perform an out-of-bounds store or
    > perform a trap.

## 5.3.1

* Remove paragraphs 4 ("The value of each character after `a`, up to and
  including `f`"),and 5 ("The value of each character after `A`, up to and
  including `F`"), and subtract 2 from paragraph numbers 6 and 7.

## 6.4.5.5

* In paragraph 3, change reference to «Table 6.5» to «Table 6.4», and renumber
  «Table 6.5» as «Table 6.4».

* In paragraph 9, change reference to «Table 6.6» to «Table 6.5», and renumber
  «Table 6.6» as «Table 6.5».

## 6.5.16

* In paragraph 10, change reference to «Table 6.7» to «Table 6.6», and renumber
  «Table 6.7» as «Table 6.6».

## 6.7.3.4

* In paragraph 16 ("EXAMPLE 4"), change «Note, however, that if» to «If».

## 6.7.13.1

* In paragraph 5, change reference to «Table M.??[]» to «Table M.1».

## 6.10.10.2

* In paragraph 1, for the macro **`__STDC_VERSION__`**, change «`202ymmL`» to
  «`202311L`».

## 6.10.10.4

* In paragraph 1, for the macros **`__STDC_IEC_60559_BFP__`**,
  **`__STDC_IEC_60559_DFP__`**, **`__STDC_IEC_60559_COMPLEX__`**,
  **`__STDC_IEC_60559_TYPES__`**, and **`__STDC_LIB_EXT1__`**, change
  «`202ymmL`» to «`202311L`».

* In paragraph 2 ("NOTE"), change «`202ymmL`» to «`202311L`».

## 7.1.2

* In paragraph 6 ("Some standard headers …"), change « which expands to
  `202311L`, where `XXXX` is the all-caps spelling of the corresponding header
  `<xxxx.h>`.» to «, where `XXXX` is the all-caps spelling of the corresponding
  header `<xxxx.h>`. These version macros expand to one of many values detailed
  in the subclauses of Annex M such as `202311L`.».

## 7.12.18.1

* In paragraph 1, where «*real-floating*» has a line-break at the hyphen, note
  that the hyphen is significant, and not just a line-breaking hyphen.

## F.1

* In paragraph 3, change «`202ymmL`» to «`202311L`».

* In paragraph 4, change «`202ymmL`» to «`202311L`».

## H.1

* In paragraph 2, change «`202ymmL`» to «`202311L`».

## I.2

* In paragraph 1, in the 3rd list item ("An implicit narrowing conversion"),
  change the section cross-reference «6.3.1» to «6.3». (This may be an error in
  the published standard.)

## J.6.2

* In paragraph 1, remove the number «53» and replace it with an ugly paragraph
  break. (This may be an error in the published standard.) Also, sort the list
  of regular expressions in ASCII order.

* In paragraph 2, remove the number «824» and replace it with an ugly paragraph
  break. (This may be an error in the published standard.) Also, sort the list
  of identifiers or keywords in case-insensitive alphanumeric order with
  underscores sorted after letters.

## J.6.3

* In paragraph 1, remove the number «1236» and replace it with an ugly paragraph
  break. (This may be an error in the published standard.) Also, sort the list
  of identifiers into case-insensitive alphanumeric order, but with underscore
  `_` sorting before end of string (for example, `abort_handler_s` appears
  before `abort`, and `BOOL_WIDTH` appears before `bool`).

## K.3.1.1

* In footnote 454, remove the parenthesized word «(potentially)».

## L.

* Remove section L.2 ("Definitions") and its subsections. Renumber section «L.3»
  ("Requirements") as «L.2».

## M.1

* In paragraph 1, change the reference to section «M.3» to «M.2».

## M.

* Remove section M.2 ("Sixth Edition") and subtract .1 from the succeeding
  sections «M.3» through «M.7».

