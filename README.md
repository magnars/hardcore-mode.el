# hardcore-mode.el

Entering hardcore-mode will disable arrow keys, backspace and return.

* Use C-f/b/n/p instead of right/left/up/down
* Use C-h instead of backspace
* Use C-m or C-j instead of return

To use C-h instead of backspace, you might need to redefine C-h:

    ;; Use shell-like backspace C-h, rebind help to F1
    (define-key key-translation-map [?\C-h] [?\C-?])
    (global-set-key (kbd "<f1>") 'help-command)

If hardcore-mode is too hardcore for you, you can add these before
you require the mode:

    (setq too-hardcore-backspace t)
    (setq too-hardcore-return t)
    (require 'hardcore-mode)
    (global-hardcore-mode)

These are the settings I am using at the time. Still not hardcore enough. ^^

## License

Copyright (C) 2011 Magnar Sveen

Author: Magnar Sveen <magnars@gmail.com>
Keywords: marking region

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
