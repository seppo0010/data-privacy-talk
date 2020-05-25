# Data Privacy talk

![Creative Commons Attribution-ShareAlike 4.0 International](cc-by-sa.svg)

The goal of this repository is to help me build a talk about data privacy.

## Subject, cases

### [Differential privacy](https://en.wikipedia.org/wiki/Differential_privacy)

* [Randomized Response: A Survey Technique for Eliminating Evasive Answer Bias](https://www.tandfonline.com/doi/abs/10.1080/01621459.1965.10480775)

* [The Tracker: A Threat to Statistical Database Security](http://www.dbis.informatik.hu-berlin.de/fileadmin/lectures/SS2011/VL_Privacy/Tracker1.pdf)

* [New Algorithms for Preserving Differential Privacy](http://reports-archive.adm.cs.cmu.edu/anon/anon/home/ftp/2010/CMU-CS-10-135.pdf)

### [De-anonymization](https://en.wikipedia.org/wiki/Data_re-identification)

* [Broken Promises of Privacy: Responding to the Surprising Failure of Anonymization](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1450006)

* [How To Break Anonymity of the Netflix Prize Dataset](https://arxiv.org/abs/cs/0610105)

* [Doe v. Netflix](https://www.wired.com/images_blogs/threatlevel/2009/12/doe-v-netflix.pdf)

* [The "Re-identification" of Governor William Weld's Medical](https://fpf.org/wp-content/uploads/The-Re-identification-of-Governor-Welds-Medical-Information-Daniel-Barth-Jones.pdf)

* [Learning to Succeed while Teaching to Fail: Privacy in Closed Machine Learning Systems](https://arxiv.org/abs/1705.08197)
  [Learning to Collaborate for User-Controlled Privacy](https://arxiv.org/abs/1805.07410)
  [Semi-supervised Knowledge Transfer for Deep Learning from Private Training Data](https://arxiv.org/abs/1610.05755)
  [Privacy Preserving Face Recognition Utilizing Differential Privacy](https://arxiv.org/abs/2005.10486)
  [Machine Learning Challenges and Opportunities of Computational Behavioral Phenotyping in Developmental Health](https://tv.vera.com.uy/video/54702)

### [Habeas data](https://en.wikipedia.org/wiki/Habeas_data)

* [Protección de los datos personales (Argentina)](http://servicios.infoleg.gob.ar/infolegInternet/anexos/60000-64999/64790/norma.htm)

* [Right of access (GDPR)](https://gdpr-info.eu/art-15-gdpr/))

* [California Consumer Privacy Act](https://oag.ca.gov/privacy/ccpa)

* [Biometric Information Privacy Act (Illinois)](http://www.ilga.gov/legislation/ilcs/ilcs3.asp?ActID=3004&ChapterID=57)
  [Patel v. Facebook](https://cases.justia.com/federal/appellate-courts/ca9/18-15982/18-15982-2019-08-08.pdf?ts=1565283704)
  [Rivera et al v. Google LLC](https://law.justia.com/cases/federal/district-courts/illinois/ilndce/1:2016cv02714/323329/207/)

## Order

Netflix privacy policy:

> We use information to provide, analyze, administer, enhance and personalize our services and marketing efforts, to manage member referrals, to process your registration, your orders and your payments, and to communicate with you on these and other topics. For example, we use such information to:
> ...
> analyze and understand our audience, improve our service (including our user interface experiences) and optimize content selection, recommendation algorithms and delivery

Netflix Prize: open competition for the best collaborative filtering algorithm to predict user ratings for films, based on previous ratings without any other information about the users or films.

How To Break Anonymity of the Netflix Prize Dataset, De-anonimization

Doe v Netflix

Habeas data, Protección de los datos personales, GDPR,  CCPA, BIPA.

Patel v Facebook, Rivera et al v Google.

Broken Promises of Privacy, The Tracker.

Differential privacy

Algorithms for differential privacy

Randomized response

Privacy Preserving Face Recognition

Privacy in Closed ML Systems

## Script (Spanish)

La gente que se crea una cuenta en Netflix accede a sus políticas de privacidad,
la mayoría de las veces sin leerlas creo, pero resulta que tiene algo de
información que vale la pena conocer.

Las políticas de privacidad, en general, tienen que brindar qué información
cede el usuario, qué recolecta la empresa, y cómo se va a usar. Si se usa de
otra forma la empresa estaría en falta. A todos nos parecería mal, por ejemplo,
que Netflix averigüe nuestra orientación sexual y la publique.

En sus términos Netflix incluye la posibilidad de usar los datos para entender
al público y mejorar sus algoritmos de recomendación. Un objetivo razonable y,
por qué no, noble.

De hecho Netflix estaba conforme con su algoritmo, pero se le ocurrió que podía
ser mejorado e hizo un concurso con premios a quienes lo mejores. Publicaron
un _data set_ con un identificador de usuario, identificador de película,
puntaje y fecha en que se puso el puntaje. Sólo con esa información hubieron
investigadores capaces de de-anonimizar usuarios cruzandolos contra la base
de datos de IMDb. En IMDb uno puede también rankear películas que vio pero
públicamente, y de esta forma se puede cruzar contra el _dataset_ publicado
que puede tener además de películas públicamente punteadas unas que se deseen
que se mantenga en privado.

La pregunta que queda por hacerse es si existe alguna información privada
que pueda ser obtenida de estos datos, una vez de-anonimizados. Y la respuesta,
según el caso Doe v. Netflix, es que sí. El interés de esta mujer en películas
del género "Gay y lesbianas" pretendía mantenerse en secreto.

Las políticas de privacidad de Netflix le permitían mejorar su algoritmo de
recomendación, sí, pero no publicar la orientación sexual de sus clientes.

Las políticas de privacidad son un requerimiento legal. Cada página debe
publicar qué datos guarda y cómo los va a usar, y no puede usarlos de otra
forma. En Argentina esto está impuesto por la Ley 25.326, Protección de Datos
Personales. De hecho también le da acceso a las personas reflejadas en la base
de datos a presentar un Habeas Data para obtener toda la información que una
empresa tiene de una, y de pedir una rectificación si hay algún error.

Para los ciudadanos de la Unión Europea el GDPR en su artículo 15 también
garantiza este derecho. En Estados Unidos no existe una ley federal para esto,
pero sí está en varios estados, por ejemplo la California Consumer Privacy Act.
En Illinois además tienen una ley que defiende la privacidad de los datos
biométricos. Facebook y Google sufrieron juicios bajo esta ley con resultados
mezclados.

Ahora si queremos cumplir con las leyes y liberar datos anonimizados, ¿cómo
hacemos? La respuesta corta es que no se puede. En el caso de Netflix se ve
como se puede cruzar la información contra una base de datos pública para
obtener información que debía mantenerse privada. Con la abundancia de datos
públicos cada vez parece más fácil esto.

En Estados Unidos 87% de las personas pueden ser identificadas sólo con código
postal, fecha de nacimiento (incluído año) y género. En 1997 el estado de
Massachusetts liberó los registros médicos de los empleados públicos y una
persona usó estas tres columnas para encontrar el correspondiente al
gobernador y demostrar así la poca seguridad de publicar información
anonimizada.

Una alternativa para ofrecer acceso a información recolectada es permitir
hacer consultas agregadas de resultados, por ejemplo contar la cantidad de
personas que vieron una película, o el promedio de puntaje que le dieron.
