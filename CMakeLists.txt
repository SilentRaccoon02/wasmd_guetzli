cmake_minimum_required(VERSION 3.5)

project(wasmd_guetzli LANGUAGES CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(sources
guetzli.cc
guetzli/butteraugli.cc
guetzli/butteraugli.h
guetzli/butteraugli_comparator.cc
guetzli/butteraugli_comparator.h
guetzli/color_transform.h
guetzli/comparator.h
guetzli/dct_double.cc
guetzli/dct_double.h
guetzli/debug_print.cc
guetzli/debug_print.h
guetzli/entropy_encode.cc
guetzli/entropy_encode.h
guetzli/fast_log.h
guetzli/fdct.cc
guetzli/fdct.h
guetzli/gamma_correct.cc
guetzli/gamma_correct.h
guetzli/idct.cc
guetzli/idct.h
guetzli/jpeg_bit_writer.h
guetzli/jpeg_data.cc
guetzli/jpeg_data.h
guetzli/jpeg_data_decoder.cc
guetzli/jpeg_data_decoder.h
guetzli/jpeg_data_encoder.cc
guetzli/jpeg_data_encoder.h
guetzli/jpeg_data_reader.cc
guetzli/jpeg_data_reader.h
guetzli/jpeg_data_writer.cc
guetzli/jpeg_data_writer.h
guetzli/jpeg_error.h
guetzli/jpeg_huffman_decode.cc
guetzli/jpeg_huffman_decode.h
guetzli/order.inc
guetzli/output_image.cc
guetzli/output_image.h
guetzli/preprocess_downsample.cc
guetzli/preprocess_downsample.h
guetzli/processor.cc
guetzli/processor.h
guetzli/quality.cc
guetzli/quality.h
guetzli/quantize.cc
guetzli/quantize.h
guetzli/score.cc
guetzli/score.h
guetzli/stats.h
)

add_executable(${PROJECT_NAME} ${sources})

add_subdirectory(libpng)

target_link_libraries(${PROJECT_NAME} png_static)
