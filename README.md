# scrrznrc
Modified version of the EGSnrc user code SPRRZnrc to calculate stopping-to-Cherenkov emission (CE) power ratios, i.e., dose-to-CE ratios under some reference conditions provided to the code. In the currect commit these are, for example: the index of refraction (hardcoded as n = 1.34 for water at room temperature and 400-600 nm, where optical absorption in water is at a minimum) and the CE polar angle aperture relative to the beam (included as an input via relevant changes in scrrznrc.mortran and the accompanying input file phsp_scrrznrc.egsinp). 

CE power is the Cherenkov photon spectral density per emitting charged particle path length (in units of photons / eV / cm). It is scored by summing contributions from charged particle steps on the fly. The code outputs to the .egslst file: dose per incident fluence and dose-to-CE ratios as energy deposited per CE photon spectral density at n = 1.34 and within the input polar angle aperture (in units of MeV eV / photon).

The version of EGSnrc at the time of the modifications can be found here: https://github.com/nrc-cnrc/EGSnrc/tree/77e3bc9aa59390641b66aeeed69b36c1bbfcc19f and the version of SPRRZnrc on which modifications were done is at: HEN_HOUSE/user_codes/sprrznrc/.

Details on the implementation are provided in comments to the code. Details of the theory, code design, testing, and relative experimental validation are available in:
Y. Zlateva, B. Muir, I. El Naqa, and J. Seuntjens, Cherenkov emission-based external radiotherapy dosimetry: I. Formalism and feasibility, Med Phys. In Print.
