
# Various force fields, in both gromacs and Amber format.

I've collated these force fields for my own use. You should check them yourself before you use them.

Chromophore force fields are included in amber03-star, amber03w and amber03ws

For CHARMM force fields, please see [Alex Mackerell's website](http://mackerell.umaryland.edu/charmm_ff.shtml). I check it periodically and update the local one accordingly.

## AMBER:

#### Installation

`amber_format/dat/leap`... basically this stuff needs to go into the corresponding dat/leap folder of your amber installation.
e.g. for Amber 14, do a git pull and then do something like `cp -r amber_format/dat/leap TARGET_DIR/amber14/dat`.

The force fields are:

**ff03x:** amber ff03* ([Best, Hummer, JPCB 2009](http://pubs.acs.org/doi/abs/10.1021/jp901540t))
**ff99SBx:** amber ff99SB* ([Best, Hummer, JPCB 2009](http://pubs.acs.org/doi/abs/10.1021/jp901540t))
**ff99SBxildn:** amber ff99SB*-ILDN ([Best, Hummer, JPCB 2009](http://pubs.acs.org/doi/abs/10.1021/jp901540t) and Lindorff-Larsen et al, Proteins, 2011 for ILDN part)
**ff03w:** amber ff03w ([Best, Mittal, JPCB, 2010](https://www.ncbi.nlm.nih.gov/pubmed/20536262))
**ff03ws:** amber ff03ws ([Best, Zheng, Mittal, JCTC 2014](https://www.ncbi.nlm.nih.gov/pubmed/25400522))

**Note** that for most, one just does a "source leaprc.ff03x" in leap, e.g., to use ff03*. To use ff03ws requires a
two-step setup described in the README for the amber force fields.

### GROMACS:

#### My additions:
**amber99sb-disp:** Amber ff99SB-disp (UNTESTED IMPLEMENTATION based on amber99sb-star-ildn-q below) (Robustelli, Piana and Shaw, PNAS, 115 (21) E4758-E4766, 2018)
**charmm22star:** Charmm 22* (Biophys J. 2011 May 4;100(9):L47-9. doi: 10.1016/j.bpj.2011.03.051.)
**charmm36m:** Charmm 36m (Mirror of http://mackerell.umaryland.edu/charmm_ff.shtml)

#### From bestlab:
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
