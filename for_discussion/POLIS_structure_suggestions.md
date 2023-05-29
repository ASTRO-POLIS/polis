# Level 1

## Observing site 

This is the lowest level of 3 layers of nesting for the observatory/telescope/instrument database we are currently compiling. The observing site itself will have the types defined previously by the StarCluster team (e.g. Ground based, space based, balloon etc.). We concentrate firstly on ground based observatories with the following tags. Follow up editions of this document for other types of observatory will be presented soon.

- **Official name:** (Official name of the observatory e.g. Siding springs, Paranal etc.)
- **Type:** Fixed, ground-based observatory
- **Place:** (The address of the Observatory, with postcode and country)
- **Longitude:** (Longitude for ground based objects, in degrees e.g. 171.93735 deg)
- **Latitude:** (Latitude for ground based objects, in degrees e.g. -42.8926 deg)
- **Contact(s):** (Usually an email if the observatory has an official contact point, or a web address. **Note: No personal email addresses!**)

***Suggestions***
- **Altitude:** (in metres above sea level)
- **Average seeing:** (in arcsec, this is usually only given for the more professional observatories)
- **Average clear nights per year:** (in days per year)
- **Light levels/pollution** (Can be defined as either the magnitude of the faintest star with real time exposure or mag/sq arcsec)
    - real time exposure limit
    - mag/sq arcsec for long exposures
- **Owner/collaborator/organisation** (who owns or is responsible for the observatory e.g. Paranal -> European Southern Observatory/ESO)
- **Access/observing restrictions** (I.e. do you need a medical check for severe altitude, do you need permission from the organisation, no access to open land during observations etc)
- **Land owner**? (in the case of indigenous land rights in Australia/Hawaii/New Zealand or other cases)


# Level 2

## Telescope 

This is the next nested layer up, i.e. for each Observing site, you go a level deeper to the telescope(s) available on each site (e.g. Optical class telescope, radio class telescope). Each telescope should have a name (or at least something like -> MEADE 16") and the tags give the basic information for each telescope. The name of each telescope will act as the starting point, with the EM spectrum coverage acting as a tag to sort out which types of telescope are available when using search or filter functions. There may be some sub-nesting depedendent on the telescope type (e.g. some types of sub-mm/radio telescopes have specific properties in certain sub-categories).

- **Gamma-ray telescope name**
    - **Electromagnetic spectrum coverage (i.e. optical, IR, radio etc)**
    - **Telescope type: Multilayer mirror/Wolter**
        - Focal length
        - Outermost mirror radius
        - Focal point
    
    - **Telescope type: Laue Lens**
    
    - **Telescope type: Compton**
    
    - **Telescope type: Cherenkov telescope**
    

- **X-ray Telescope Name**
    - **Electromagnetic Spectrum Coverage (i.e. optical, IR, Radio etc)**
    - **Telescope type: Wolter Type I**
        - Focal length
        - Outermost mirror radius
        - Focal point
        
    - **Telescope type: Wolter Type II**
        - Focal length
        - Outermost mirror radius
        - Focal point
        
    - **Telescope type: Wolter Type III**
        - Focal length
        - Outermost mirror radius
        - Focal point


- **UV telescope name**
    - **Electromagnetic spectrum coverage:** (i.e. optical, IR, radio etc can also be multiple such as Hubble has UV/Optical/NIR)
    
    - **Telescope type: Reflector** (Pre-defined type)
        - **Reflective design:** (options given here)
            - Newtonian
            - Cassegrain
            - Gregorian
            - Ritchey-Chretien
            - Rectangular
            - Rowland circle
        
    - **Aperture:** (This should be in metres, e.g. 0.1m)
    - **Focus** (options given here)
        - Prime focus
        - Nasmyth
        - Coude
        - Cassegrain
    - **Focal length** (in metres)
    - **Focal ratio** (state the f/x number)
    - **Manufacturer** (This list will need constantly updating as the project develops)
        - Astrosysteme Austria
        - Celestron
        - Meade
        - Other (extra information given by user)
    - **Mirror coating** (options given here)
        - Gold
        - Aluminium
        - Silver
        
    - **Mount**
        - **Type** (options given here)
            - German equitorial
            - Fork 
            - Yoke 
            - Horseshoe
            - Cross-axis
            - Dobsonian
            - Altitude-Azimuth
            - Zenith
            - Polar
        - **Manufacturer** (This list will need constantly updating as the project develops)
            - Astrosysteme Austria
            - Celestron
            - Meade
            - Other (extra information given by user)

- **Optical telescope name**
    - **Electromagnetic spectrum coverage:** (i.e. optical, IR, radio etc can also be multiple such as Hubble has UV/Optical/NIR)
    
    - **Telescope type: Refractor**
        - **Refractive design:** (options given here)
            - Galilean
            - Keplerian
            - Achromatic
            - Apochromatic
            - Other (extra information given by user)
            
    - **Telescope type: Reflector**
        - **Reflective design:** (options given here)
            - Newtonian
            - Cassegrain
            - Gregorian
            - Ritchey-Chretien
            - Schmidt
            - Dall-Kirkham
            - Liquid Mirror
            - Maksutov
            - Other (extra information given by user)
        
    - **Focus** (options given here)
        - Newtonian
        - Prime focus
        - Nasmyth
        - Coude
        - Cassegrain

    - **Aperture:** (This should be in metres, e.g. 0.1m)
    - **Focal length:** (in metres)
    - **Focal ratio:** (give the f/x number)
    - **Manufacturer** (This list will need constantly updating as the project develops)
        - Astrosysteme Austria
        - Celestron
        - Meade
        - Other (extra information given by user)
    - **Mirror coating** (options given here)
        - Gold
        - Aluminium
        - Silver

    - **Mount**
        - **Type** (options given here)
            - German equitorial
            - Fork 
            - Yoke 
            - Horseshoe
            - Cross-axis
            - Dobsonian
            - Altitude-Azimuth
            - Zenith
            - Polar
        - **Manufacturer** (This list will need constantly updating as the project develops)
            - Astrosysteme Austria
            - Celestron
            - Meade
            - Other (extra information given by user)
            
    - **Adaptive optics**
        - **Type** (options given here)
            - Narrow-field
            - Wide-field
        - **Wavefront sensor** (options given here)
            - Shack-Hartmann
            - Curvature sensor
            - Pyramid sensor
            - Other (user defined)
        - **Guide star** (can be both or just a natural guide star)
            - Laser
            - Natural guide star

- **IR Telescope Name**
    - **Electromagnetic spectrum coverage:** (i.e. optical, IR, Radio etc can also be multiple such as Hubble has UV/Optical/NIR)
    
    - **Telescope type: Reflector**
        - **Reflective type**  (options given here, may need updating)
            - Newtonian
            - Cassegrain
            - Gregorian
            - Ritchey-Chretien
            - Schmidt
            
    - **Focus** (options given here)
        - Newtonian
        - Prime focus
        - Nasmyth
        - Coude
        - Cassegrain
        
    - **Aperture:** (This should be in metres, e.g. 0.1m)
    - **Focal length:** (in metres)
    - **Focal ratio:** (give the f/x number)
    - **Manufacturer** (This list will need constantly updating as the project develops)
        - Astrosysteme Austria
        - Celestron
        - Meade
        - Other (extra information given by user)
    - **Mirror coating** (options given here)
        - Gold
        - Aluminium
        - Silver
        
    - **Mount**
        - **Type** (options given here)
            - German equitorial
            - Fork 
            - Yoke 
            - Horseshoe
            - Cross-axis
            - Dobsonian
            - Altitude-Azimuth
            - Zenith
            - Polar
        - **Manufacturer** (This list will need constantly updating as the project develops)
            - Astrosysteme Austria
            - Celestron
            - Meade
            - Other (extra information given by user)

- **Sub-mm telescope name**
    - **Electromagnetic spectrum coverage:** (i.e. Sub-mm, radio etc.)
    - **Telescope type: Steerable dish**
        - **Diameter** (in metres)
        - **Dish type** (options given here)
            - Fixed Parabolic
            - Homologous (deformable parabolic)
        - **Focus** (options given here)
            - Prime focus on-axis
            - Prime focus off-Axis
            - Gregorian
            - Cassegrain
            - Offset Cassegrain
            - Dual offset
            - Naysmith 
        - **Focal length** (in metres)
        - **Focal ratio** (give the f/x number)
        - **Manufacturer** (This list will need constantly updating as the project develops)
            - Astrosysteme Austria
            - Celestron
            - Meade
            - Other (extra information given by user)
        - **Array** (yes/no, options given here)
            - Number of constituents
            - Minimum Baseline
            - Maximum Baseline
        - **VLBI capabilities** (yes/no, options given here)
            - Parent network
            - Number of other constituents
            - Maximum Baseline
            
    - **Telescope type: Reflector**
        - **Aperture:** (This should be in metres, e.g. 0.1m)
        - **Reflective design:** (options given here)
            - Newtonian
            - Cassegrain
            - Gregorian
            - Ritchey-Chretien
        - **Focus** (options given here)
            - Prime focus
            - Nasmyth
            - Coude
            - Cassegrain
        - **Focal length** (in metres)
        - **Focal ratio** (give the f/x number)
        - **Manufacturer** (This list will need constantly updating as the project develops)
            - Astrosysteme Austria
            - Celestron
            - Meade
            - Other (extra information given by user)
        
    - **Mount**
        - **Type** (options given here)
            - German equitorial
            - Fork 
            - Yoke 
            - Horseshoe
            - Cross-axis
            - Dobsonian
            - Altitude-Azimuth
            - Zenith
            - Polar
        - **Manufacturer** (This list will need constantly updating as the project develops)
            - Astrosysteme Austria
            - Celestron
            - Meade
            - Other (extra information given by user)

- **Radio telescope name**
    - **Electromagnetic spectrum coverage:** (i.e. Sub-mm, Radio etc)
    - **Telescope type: Steerable dish**
        - **Diameter** (in metres)
        - **Dish type** (options given here)
            - Fixed Parabolic
            - Homologous (deformable parabolic)
        - **Focus** (options given here)
            - Prime focus on-axis
            - Prime focus off-Axis
            - Gregorian
            - Cassegrain
            - Offset Cassegrain
            - Dual offset
            - Naysmith 
        - **Focal length** (in metres)
        - **Focal ratio** (give the f/x number)
        - **Manufacturer**
        - **Array** (yes/no)
            - Number of constituents
            - Minimum Baseline
            - Maximum Baseline
        - **VLBI capabilities** (yes/no)
            - Parent network
            - Number of other constituents
            - Maximum Baseline
        
    - **Telescope type: Static dish**
        - **Diameter**
        - **Effective diameter**
        - **Dish type**
            - Fixed Parabolic
            - Fixed Spherical
            - Cylindrical Paraboloid
        - **Focus**
            - Steerable Prime focus
        - **Focal length**
        - **Focal ratio**
        - **Manufacturer**
        - **Wavelength range**
        - **Frequency range**
        - **Array** (yes/no)
            - Number of constituents
            - Minimum Baseline
            - Maximum Baseline
        - **VLBI capabilities** (yes/no)
            - Parent network
            - Number of other constituents
            - Maximum Baseline
    
    - **Antenna**
        - **Antenna span**
        - **Effective diameter/baseline**
        - **Manufacturer**
        - **Polarisation**
            - Dual
            - Linear
        - **Array** (yes/no)
            - Number of constituents
            - Minimum Baseline
            - Maximum Baseline
        - **VLBI capabilities** (yes/no)
            - Parent network
            - Number of other constituents
            - Maximum Baseline
        
    - **Mount**
        - **Type** (options given here)
            - German equitorial
            - Fork 
            - Yoke 
            - Horseshoe
            - Cross-axis
            - Dobsonian
            - Altitude-Azimuth
            - Zenith
            - Polar
        - **Manufacturer** (This list will need constantly updating as the project develops)
            - Astrosysteme Austria
            - Celestron
            - Meade
            - Other (extra information given by user)


# Level 3

## Instrument/Detector

- **CCD camera**
    - **Semi-conductor material**
    - **Pixel scale**
    - **Pixel number**
    - **Filters**
        - e.g. SDSS u,g,r,i,z
        - e.g. Johnson B,V etc
    - **Manufacturer**

- **Spectrograph**
    - **Type of Spectrograph**
        - Longslit
        - Single Fibre
        - Multi-slit
        - Multi-Fibre
        - IFU
    - **Wavelength range**
    - **Resolution**
        - Minimum (wavelength)
        - Maximum (wavelength)
    - **Type of dispersion unit**
        - Echelle
        - Grism
        - Prism
        - Grating
        - Other (User defined)
    - **Manufacturer**

- **Photographic plate**
    - **Name** (Equivilent to filter band)
    - **Material**
    - **Wavelength limit**
    - **Grain-size**
    - **Manufacturer**

- **CMOS camera**
    - **Semi-conductor material**
    - **Pixel scale**
    - **Pixel number**
    - **Filters**
        - e.g. SDSS u,g,r,i,z
        - e.g. Johnson B,V etc
    - **Manufacturer**

- **Photomultiplier tube**
    - **Material**
    - **Gain Factor**
    - **Electric field voltage**
    - **Wavelength range**

- **Bolometer**
    - **Material**
    - **Wavelength range**
    - **Pixel number**
    - **Pixel scale**
    
- **Sub-mm/Radio recievers**
        - **Wavelength range**
            - Bands (Bandwidth)
        - **Frequency range**
            - Bands (Bandwidth)
    
- Submm: Heterodyne recievers
    
- X-ray: Proportional counter

- X-ray: Scintillation Counter

- X-ray: Microchannel plates

- Gamm-ray: Solid state (CCD equivilent)

- Gamma-ray: Pair-creation

- Gamma-ray: Air Cherenkov
