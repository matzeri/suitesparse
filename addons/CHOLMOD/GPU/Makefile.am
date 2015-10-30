AM_CPPFLAGS = -I$(top_srcdir)/Include @SUITESPARSECONFIG_CFLAGS@ 

noinst_LTLIBRARIES = libgpu.la libgpul.la
noinst_HEADERS = \
	t_cholmod_gpu.c 

libgpu_la_SOURCES = \
	cholmod_gpu.c \
	cholmod_gpu_kernels.c 
libgpu_la_LIBADD = @BLAS_LIBS@ @LAPACK_LIBS@ @CUBLAS_LIBS@

libgpul_la_CPPFLAGS = $(AM_CPPFLAGS) -DDLONG
libgpul_la_SOURCES = $(libgpu_la_SOURCES)
libgpul_la_LIBADD = $(libgpu_la_LIBADD)

EXTRA_DIST = cholmod_gpu_kernels.cu
