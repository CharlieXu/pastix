all: reg_axpy reg_copy reg_geam reg_gemm reg_pof reg_ppf reg_scal reg_trsm reg_gemv reg_trsv

reg_axpy: reg_axpy.c num_rec
	gcc -o reg_axpy reg_axpy.c num_recipes/*.o -Inum_recipes/ -lm

reg_copy: reg_copy.c num_rec
	gcc -o reg_copy reg_copy.c num_recipes/*.o -Inum_recipes/ -lm

reg_geam: reg_geam.c num_rec
	gcc -o reg_geam reg_geam.c num_recipes/*.o -Inum_recipes/ -lm

reg_gemm: reg_gemm.c num_rec
	gcc -o reg_gemm reg_gemm.c num_recipes/*.o -Inum_recipes/ -lm

reg_pof: reg_pof.c num_rec
	gcc -o reg_pof reg_pof.c num_recipes/*.o -Inum_recipes/ -lm

reg_ppf: reg_ppf.c num_rec
	gcc -o reg_ppf reg_ppf.c num_recipes/*.o -Inum_recipes/ -lm

reg_scal: reg_scal.c num_rec
	gcc -o reg_scal reg_scal.c num_recipes/*.o -Inum_recipes/ -lm

reg_trsm: reg_trsm.c num_rec
	gcc -o reg_trsm reg_trsm.c num_recipes/*.o -Inum_recipes/ -lm

reg_gemv: reg_gemv.c num_rec
	gcc -o reg_gemv reg_gemv.c num_recipes/*.o -Inum_recipes/ -lm

reg_trsv: reg_trsv.c num_rec
	gcc -o reg_trsv reg_trsv.c num_recipes/*.o -Inum_recipes/ -lm

num_rec: covsrt.o gaussj.o lfit.o nrutil.o num_recipes/nr.h num_recipes/nrutil.h num_recipes/complex.h

covsrt.o: num_recipes/covsrt.c
	gcc -o num_recipes/covsrt.o -c num_recipes/covsrt.c

gaussj.o: num_recipes/gaussj.c
	gcc -o num_recipes/gaussj.o -c num_recipes/gaussj.c

lfit.o: num_recipes/lfit.c
	gcc -o num_recipes/lfit.o -c num_recipes/lfit.c

nrutil.o: num_recipes/nrutil.c
	gcc -o num_recipes/nrutil.o -c num_recipes/nrutil.c

clean:
	rm -rf *.o num_recipes/*.o
