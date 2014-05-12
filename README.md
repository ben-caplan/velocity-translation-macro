velocity-translation-macro
==========================

dotCMS Velocity Translation Macros

Suggested Use
==
First you will need to include this VTL

  #dotParse( '[PATH]/velocity-translation-macro.vtl' )##
  
With the macro included, can now set up some country specific variables:
  
  #addTranslation('FR' 'obsessedWithTech' 'Ici Et Ailleurs')##
  #addTranslation('US' 'obsessedWithTech' 'Obsessed with Technology')##
  #addTranslation('JP' 'obsessedWithTech' 'サービスのご案内')##
  #addTranslation('NL' 'obsessedWithTech' 'Global Reach')##
  
Now all you need to do is call the relevant translation to the page:

  #set( $pageLang = 'FR' )## only set this one once. 
  #translate( 'obsessedWithTech' $pageLang )##
  
  ## OR if you don't want a US fall back:
  #translate( 'obsessedWithTech' $pageLang true )##
  
Happ coding :-)
