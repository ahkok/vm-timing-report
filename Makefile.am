# declare vars
AM_CFLAGS = -std=gnu99 -fstack-protector -Wall -pedantic \
        -Wstrict-prototypes -Wundef -fno-common \
        -Werror-implicit-function-declaration \
        -Wformat -Wformat-security -Werror=format-security \
	-Wconversion -Wunreachable-code

bin_PROGRAMS = \
	vm-timing-report

bin_SCRIPTS = \
	scripts/spin-from-raw.sh \
	scripts/gen-ubuntu-rawfs.sh

supportdir = $(datadir)/vm-timing-report
support_DATA = \
	scripts/vm-report.sh \
	data/vm-report.service \
	data/vm-report.init

vm_timing_report_SOURCES = \
	src/vm-timing-report.c

vm_timing_report_CFLAGS = \
	$(AM_CFLAGS)

vm_timing_report_LDADD = \
	-lrt \
	-lpthread

EXTRA_DIST = \
	README.md \
	README.CentOS.md \
	LICENSE \
	scripts/vm-report.sh \
	scripts/spin-from-raw.sh \
	scripts/gen-ubuntu-rawfs.sh
	data/vm-report.init
	data/vm-report.service

