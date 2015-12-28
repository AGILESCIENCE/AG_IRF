# Instructions:
# Run 'make' or 'make install' to copy data to the prefix path.
#
# You can override the install prefix with the command:
#   make prefix="/my/install/path"

prefix=$(AGILE)

all: install

install:
	test -d "$(prefix)/model/scientific_analysis/data/" || mkdir -p "$(prefix)/model/scientific_analysis/data/"
	cp *.gz "$(prefix)/model/scientific_analysis/data/"
