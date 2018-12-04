# Hello, world!
#
# This is an example function named 'hello'
# which prints 'Hello, world!'.
#
# You can learn more about package authoring with RStudio at:
#
#   http://r-pkgs.had.co.nz/
#
# Some useful keyboard shortcuts for package authoring:
#
#   Build and Reload Package:  'Ctrl + Shift + B'
#   Check Package:             'Ctrl + Shift + E'
#   Test Package:              'Ctrl + Shift + T'

#' Function that merge based on complex key
#'
#' This function allows you to merge 2 data frames using complex keys
#' Include options for all.x, all.y and all
#' @param dp_dat1
#' @param dp_dat2
#' @param sp_complex_key1
#' @param sp_complex_key2
#' @keywords merging
#' @export
#'
complex_key_merging <- function(dp_dat1, dp_dat2, sap_complex_key1, sap_complex_key2) {

sComplexKey1 = paste(sap_complex_key1, collapse = "_")
sComplexKey2 = paste(sap_complex_key2, collapse = "_")

dData_sub1 = subset(dp_dat1, select = sap_complex_key1)
dData_sub2 = subset(dp_dat2, select = sap_complex_key2)

#Change this to
dp_dat1$complex_key1 = apply(dData_sub1, 1, paste, collapse = "_")
dp_dat2$complex_key2 = apply(dData_sub2, 1, paste, collapse = "_")

dData = merge(dp_dat1, dp_dat2, by.x = "complex_key1", by.y = "complex_key2", all.x = T)

return(dData)
}





