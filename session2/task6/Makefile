# Makefile for Task 6

CFLAGS = -g #-fsanitize=address -fno-omit-frame-pointer
EXECS = leak noleak stack_over testlogin use_after heap_over

help:
	@echo "Task 6 Help:"
	@echo
	@echo "Enter 'make' followed by name of an executable"
	@echo "(Options are: $(EXECS))"
	@echo
	@echo "Remove all executables with 'make clean'"

%: %.c
	gcc $(CFLAGS) $< -o $@

clean:
	@rm -f $(EXECS)
	@rm -rf $(patsubst %,%.dSYM,$(EXECS))   # for clang on Macs

.PHONY: clean help
