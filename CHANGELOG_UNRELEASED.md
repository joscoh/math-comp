# Changelog (unreleased)

To avoid having old PRs put changes into the wrong section of the CHANGELOG,
new entries now go to the present file as discussed
[here](https://github.com/math-comp/math-comp/wiki/Agenda-of-the-April-23rd-2019-meeting-9h30-to-12h30#avoiding-issues-with-changelog).

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

### Added

- in `bigop.v`, added lemma `leq_prod`
- in `path.v`, added lemma `sortedP`
- in `seq.v`, added statement `size_take_min`

- in `ssralg.v`
  + number notation in scope ring_scope, numbers such as `12` or `42`
    are now read as `12%:R` or `42%:R`

- in `rat.v`
  + Number Notation for numbers of the form `-? [0-9][0-9_]* ([.][0-9_]+)?`
    in scope `rat_scope` (for instance 12%Q or 3.14%Q)

- in `ssrint.v`
  + number notation in scope int_scope, `12` or `-42`
    are now read as `Posz 12` or `Negz 41`

- in `ssrint.v`
  + number notation in scope ring_scope, numbers such as `-12` are now
    read as `(-12)%:~R`

- in `bigop.v`, added lemmas `telescope_big`, `telescope_sumn` and `telescope_sumn_in`

- in `fintype.v`, added lemmas `enum_ord0`, `enum_ordSl`, `enum_ordSr`

- in `ssrbool.v`, added lemma `all_sig2_cond`
- in `choice.v`, added coercion `Choice.mixin`
- In `seq.v`, added lemmas `mkseqS`, `mkseq_uniqP`

- in `seq.v`, added lemmas `nth_seq1`, `set_nthE`, `count_set_nth`,
  `count_set_nth_ltn`, `count_set_nthF`

- in `finfield.v`, added type of polynomial quotients `qpoly` and algebraic structures:
  + canonical instances making `qpoly p` (for `p` irreducible) a `subType` `eqType`,
    `choiceType`, `countType`, `subCountType`, `finType`, `ZmodType`, `ringType`,
    `comRingType`, `unitRingType`, `comUnitRingType`, `idomainType`, `fieldType`, and
    `finFieldType`
  + added definition of `primitive_poly` and `dlog` (discrete log)
  + added lemmas `exp_dlog`, `dlog0`, `dlog_exp`, `qx_field_sz1`, and `qpoly_exp_modn1`

- in `ssrnat.v`, added lemma `leq_predR`

### Changed

- in `rat.v`
  + `zeroq` and `oneq` (hence `0%Q` and `1%Q`) are now the evaluation
    of terms `fracq (0, 1)` and `fracq (1, 1)` (and not the term
    themselves), the old and new values are convertible and can be
    easily converted with `rewrite -[0%Q]valqK -[1%Q]valqK`

- in `order.v`
  + fix `[distrLatticeType of T with disp]` notation

- in `fintype.v`
  + `enum_ordS` now a notation

### Renamed

- in `ssrbool.v`, renamed `mono2W_in` to `mono1W_in` (was misnamed).

### Removed

### Infrastructure

- in `builddoc_lib.sh`:
  + change the sed command that removes all starred lines

### Misc
