#######
#
#  `Makefile'.
#
#  This file is the makefile for the GNU dr.
#
#  Copyright (C) 2008  Efstathios Chatzikyriakidis (contact@efxa.org)
#
#  This program is free software: you can redistribute it and/or modify
#  it under the terms of the GNU General Public License as published by
#  the Free Software Foundation, either version 3 of the License, or
#  (at your option) any later version.
#
#  This program is distributed in the hope that it will be useful,
#  but WITHOUT ANY WARRANTY; without even the implied warranty of
#  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
#  GNU General Public License for more details.
#
#  You should have received a copy of the GNU General Public License
#  along with this program. If not, see <http://www.gnu.org/licenses/>.
#
#######

# information which help the install, uninstall part.

# the name of the executable program.
EXEC = gdr

# the targets.

# install man page, info page and the program.
install:
	gzip -c ../man/$(EXEC).1 > ../man/$(EXEC).1.gz
	mv -f ../man/$(EXEC).1.gz $(man_path)

	makeinfo ../texi/$(EXEC).texi -o ../texi/$(EXEC).info
	gzip -c ../texi/$(EXEC).info > ../texi/$(EXEC).info.gz
	mv -f ../texi/$(EXEC).info.gz $(info_path)

	cp -f $(EXEC) $(bin_path)

	rm -f ../texi/$(EXEC).info

# uninstall man page, info page and the program.
uninstall:
	rm -f $(man_path)/$(EXEC).1.gz
	rm -f $(info_path)/$(EXEC).info.gz
	rm -f $(bin_path)/$(EXEC)
