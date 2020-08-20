# uvwind
This github describes how to use the xspec model for the UV line driven disc wind, used in the paper "UV line driven disc wind as the origin of ultrafast outflows in AGN" (Mizumoto et al. submitted to MNRAS, https://ui.adsabs.harvard.edu/abs/2020arXiv200301137M/abstract). If you use this model in your paper, please carefully read Mizumoto et al. and cite both of Mizumoto et al. and Nomura et al. 2020, 494, 3616 (https://ui.adsabs.harvard.edu/abs/2020MNRAS.494.3616N/abstract).
This uvwind model is an atable model. You can use it as, for example, 
~~~
model atable{uvwind.fits}+atable{uvwind.fits}
~~~
where the first model is the primary component whereas the second is the scattered one.
This model covers only in 2-30 keV. the flux is set to be zero out of the region.
In this model the input spectrum is fixed to be a power law. If you would like to use this model as a mtable model, please contact Misaki Mizumoto (mizumoto.misaki.n68_at_kyoto-u.jp).

Parameters for uvwind:
* par1:   Primary compoent or scattered component. If par1=0, this model shows the primary component absorbed in the wind, whereas if par1=1, it shows the secondary component scattered on the wind out of the line of sight.
* par2:   Inclination. The range is 40+(65-40)/9*(par2-1) deg < theta < 40+(65-40)/9*(par2) deg. See the 4th paragraph in section 2.3 of Mizumoto et al.
* par3:   Photon index of the input power law
* par4:   Redshift
* norm:   Same as the one in the "powerlaw" model
