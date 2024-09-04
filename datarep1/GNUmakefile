PROGRAMS = add addu addv intgen intsort intsort-binsearch intsort-tree intsort-vector
all: $(PROGRAMS)

include ../common/rules.mk

%.o: %.cc $(BUILDSTAMP)
	$(CXX) $(CPPFLAGS) $(CXXFLAGS) $(DEPCFLAGS) $(O) -o $@ -c $<

addu addv intgen intsort intsort-binsearch intsort-tree intsort-vector: \
%: %.o print_bytes.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $(O) -o $@ $^

add: \
%: %.o addf.o print_bytes.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $(O) -o $@ $^


clean:
	rm -rf $(PROGRAMS) $(wildcard intsort[1-6]) *.o $(DEPSDIR)

.PHONY: all clean
