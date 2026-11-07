# Changelog

## [2.0.0](https://github.com/mmugi/mmerr.nvim/compare/v1.0.0...v2.0.0) (2026-11-07)


### ⚠ BREAKING CHANGES

* `highlight_overrides` is replaced by `edit_highlights(groups, palette)`, which edits the highlight groups in place instead of returning replacements.
* background colors are renamed:
    - bg_charcoal → charcoal
    - bg_gray → graphite
    - bg_dusk → twilight
    - bg_blue → koamaru

### Features

* add colors to the palette ([#5](https://github.com/mmugi/mmerr.nvim/issues/5), [#8](https://github.com/mmugi/mmerr.nvim/issues/8)) ([c5cfeb2](https://github.com/mmugi/mmerr.nvim/commit/c5cfeb2abdaa03f2f92e7bba8743f7fbb7d9840a))
* add MmerrReload command ([#18](https://github.com/mmugi/mmerr.nvim/issues/18)) ([c07e568](https://github.com/mmugi/mmerr.nvim/commit/c07e5686c8bb5318c07af09964e95683d7857873))
* **diagnostic:** use ice for hints ([#10](https://github.com/mmugi/mmerr.nvim/issues/10)) ([962acc6](https://github.com/mmugi/mmerr.nvim/commit/962acc66717f08f5bb013e84406bcca0314feb83))
* **diagnostic:** use moon for unnecessary code ([#10](https://github.com/mmugi/mmerr.nvim/issues/10)) ([962acc6](https://github.com/mmugi/mmerr.nvim/commit/962acc66717f08f5bb013e84406bcca0314feb83))
* **editor:** highlight the selected tab ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** restyle the popup menu ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** restyle the search highlights ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** restyle the statusline ([#14](https://github.com/mmugi/mmerr.nvim/issues/14)) ([d5cb56c](https://github.com/mmugi/mmerr.nvim/commit/d5cb56c5020404ad87091b23d8bbe78571446878))
* **editor:** use cyan for messages ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** use cyan on black for floating windows ([#16](https://github.com/mmugi/mmerr.nvim/issues/16)) ([d504309](https://github.com/mmugi/mmerr.nvim/commit/d504309a0efedd39a3533dacd4447f0d733cb575))
* **editor:** use folly for the cursorline ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** use gray for line numbers ([#16](https://github.com/mmugi/mmerr.nvim/issues/16)) ([d504309](https://github.com/mmugi/mmerr.nvim/commit/d504309a0efedd39a3533dacd4447f0d733cb575))
* **editor:** use green for added diff lines ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** use green for the visual selection ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** use lime for the sign column ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **editor:** use lime for titles ([#9](https://github.com/mmugi/mmerr.nvim/issues/9)) ([ee537c4](https://github.com/mmugi/mmerr.nvim/commit/ee537c4462ee2c16f4d1b8a2a35497182427c5f6))
* **lazy:** add highlights for lazy.nvim ([#17](https://github.com/mmugi/mmerr.nvim/issues/17)) ([2763448](https://github.com/mmugi/mmerr.nvim/commit/2763448414002ae4c8a763c9acb7ec97d80bf12c))
* **lsp:** use violet for references ([#11](https://github.com/mmugi/mmerr.nvim/issues/11)) ([505ccd4](https://github.com/mmugi/mmerr.nvim/commit/505ccd4c681624712eeef30170d52ae994695eca))
* make black more neutral ([#16](https://github.com/mmugi/mmerr.nvim/issues/16)) ([d504309](https://github.com/mmugi/mmerr.nvim/commit/d504309a0efedd39a3533dacd4447f0d733cb575))
* rename background colors ([#7](https://github.com/mmugi/mmerr.nvim/issues/7)) ([292c7a2](https://github.com/mmugi/mmerr.nvim/commit/292c7a23c2951e78231526345455f01f477dbf9b))
* replace highlight_overrides with edit_highlights ([#15](https://github.com/mmugi/mmerr.nvim/issues/15)) ([fbd5df6](https://github.com/mmugi/mmerr.nvim/commit/fbd5df66f209d89234ae2833fc231d93568b5341))
* **telescope:** tweak the prompt and selection colors ([#12](https://github.com/mmugi/mmerr.nvim/issues/12)) ([66a49f7](https://github.com/mmugi/mmerr.nvim/commit/66a49f71dfb6cb0dd8ab614bc5af8b6a49a61747))


### Bug Fixes

* **editor:** keep NormalFloat in unfocused floating windows ([#16](https://github.com/mmugi/mmerr.nvim/issues/16)) ([d504309](https://github.com/mmugi/mmerr.nvim/commit/d504309a0efedd39a3533dacd4447f0d733cb575))
