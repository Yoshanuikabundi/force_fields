
# Various force fields, in Gromacs format.

I don't use AMBER so my tweaks are all here.

Chromophore force fields are included in amber03-star, amber03w and amber03ws

For CHARMM force fields in Gromacs format, please see
[Alex Mackerell's website](http://mackerell.umaryland.edu/charmm_ff.shtml).
I check it periodically and update my copy of it accordingly.

## Some details:

### My additions:
**amber99sb-disp:** Amber ff99SB-disp (UNTESTED IMPLEMENTATION based on amber99sb-star-ildn-q below) (Robustelli, Piana and Shaw, PNAS, 115 (21) E4758-E4766, 2018)  
**charmm22star:** Charmm 22* (Biophys J. 2011 May 4;100(9):L47-9. doi: 10.1016/j.bpj.2011.03.051.)  
**charmm36m:** Charmm 36m (Mirror of http://mackerell.umaryland.edu/charmm_ff.shtml)  

### From bestlab:
**amber03-star:** amber ff03* (Best, Hummer, 2009)  
**amber99sb-star:** amber ff99SB* (Best, Hummer, 2009)  
**amber99sb-star-ildn:** amber ff99SB*-ILDN (Best, Hummer, 2009 and Lindorff-Larsen et al, Proteins, 2011 for ILDN part)  
**amber99sb-star-ildn-q:** amber ff99SB*-ILDN-q (same as above, but with backbone charge mods as described in Best, De Sancho, Mittal, Biophys. J. 2012)  
**amber03w:** amber ff03w (Best, Mittal, 2010)  
**amber03ws:** amber ff03ws (Best, Zheng, Mittal, 2014)  
**amber99sbw:** amber ff99SBw (ref?)  
**amber99sbws:** amber ff99SBws (Best, Zheng, Mittal, 2014 -- see the SI)  


**denaturants-amber03ws:** urea and gdmcl force fields (Zheng, Best, JCTC, 2015)


**AMBER-DYES-1.0_patched:** simple fix to original AMBER-DYES force field (Graen et al, JCTC, 2014).
- The original force field contained a rather minor and likely inconsequential
error in the covalent bonding of the maleimide-derived conjugates, which this
patch seeks to fix. Described in more detail in the containd README

### How to install?
- Copy the needed folders to your gromacs "top" directory, or to the local directory
where you are setting up your simulation.

### Which protein force field should I use?
- All force fields should give reasonable properties for folded proteins, although these
will be slightly destabilized by the 03ws and 99sbws variants. However for simulations
of intrinsically disordered or unfolded proteins, of protein-protein interactions, and
of protein-dye conjugates, it is recommended to use ff03ws or ff99sbws.

### Which chromophore force field should I use?
- For the frequently used Alexa488 and Alexa594 chromophores, the best validated
force field is the one included with amber03ws and amber99sbws and is therefore
recommended. Setup is described in the dyes_example folder one level above here.
- For other chromophores, an extensive library is provided by the patched
AMBER-DYES distribution. However, it should also be used with one of the
water-scaling force fields in order that the chromophores do not stick excessively
to the protein. Setup is described in the README and example setup script in
the AMBER-DYES-1.0_patched folder on level up.
