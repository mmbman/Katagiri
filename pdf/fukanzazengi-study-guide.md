---
//title: "Katagiri Roshi’s Teachings on _Fukanzazengi_"
//subtitle: "A Study Guide for Zen Master Dōgen’s _Universal Recommendation for Zazen_"
//author: Edited by Kikan Michael Howard. Commentary © 2026 Kikan Michael Howard. Katagiri Roshi’s talks © Minnesota Zen Meditation Center.
//date: Version 0 - March 17, 2026
#margin:
#  x: 1.0in
#  y: 1.0in
#mainfont: "Helvetica"
#mainfont: "Source Sans 3"
#mainfont: "Avenir Next"
mainfont: "Proxima Nova"
fontsize: 12pt
---
```{=typst}
//#import "@preview/hydra:0.6.0": hydra
#set document(title: [Katagiri Roshi’s Teachings on _Fukanzazengi_], author: "Kikan Michael Howard, Dainin Katagiri, Eihei Dōgen", description: [Commentary © 2026 Kikan Michael Howard. Katagiri Roshi’s talks © Minnesota Zen Meditation Center.])

//#set smartquote(enabled: false)

#align(center + horizon)[
  #text(size: 1.8em, weight: "bold")[Katagiri Roshi’s Teachings on _Fukanzazengi_]
  
  #v(1em)
  #text(size: 1.5em)[A Study Guide for Zen Master Dōgen’s #linebreak()_Universal Recommendation for Zazen_]
  
  #v(4em)
  #text(size: 1.2em)[Edited by Kikan Michael Howard]
  
  #v(4em)
  #text(size: 1.2em)[Draft Version 0.5]
  
  #datetime.today().display()
  
  #v(4em)
  #text(size: 1.2em)[Commentary © 2026 Kikan Michael Howard#linebreak()Katagiri Roshi’s talks © Minnesota Zen Meditation Center]
]

#pagebreak()

// End title page, start document content
//#set page(numbering: "1")
#counter(page).update(1)

#set page(
  header: context {
    set text(size: 11pt)
    h(1fr) 
    [_Katagiri Roshi’s Teachings on Fukanzazengi_]
    h(1fr) 
  }
)
#let current-chapter-title() = context {
  let headings = query(heading.where(level: 1).before(here()))
  if headings == () { panic("At least one heading must be defined.") }
  headings.last().body
}
#set page(
  footer: context {
    set text(size: 11pt)
//    line(length: 100%, stroke: 0.5pt)
    let page-num = counter(page).get().first()
    if calc.even(page-num) {
      current-chapter-title()
      //hydra(1)
      h(1fr)
      [#page-num]
    } else {
      [#page-num]
      h(1fr)
      current-chapter-title()
    }
  }
)
//#set page(
//  footer: context {
//    let page-num = counter(page).get().first()
//      [#page-num]
//      h(1fr)
//      current-chapter-title()
//  }
//)
#outline(depth: 1)
#pagebreak()
```

# Introduction 

Zen Master Dōgen’s *Fukanzazengi* (“Universal Recommendation for Zazen”) is probably the most fundamental text of Sōtō Zen Buddhism. Composed by Eihei Dōgen in 13th century Japan, written in Classical Chinese, it explains both the *how* and the *why* of Zen meditation. Traditionally this short text is recited every evening during *sesshin* (Zen meditation retreat), but it has meaning for practitioners in all areas of life – hence “*Universal* Recommendation.”
 
Dainin Katagiri Roshi, the founder of Sōtō Zen in Minnesota, worked for decades to bring Dōgen Zenji’s teachings to English-speaking Americans, giving hundreds of dharma talks at [Minnesota Zen Meditation Center](https://www.mnzencenter.org/katagiri-project.html). In this document, I go through *Fukanzazengi* line-by-line and attempt to bring together Katagiri Roshi’s teachings on each part of the text, drawn from many of his different talks over the years from 1979 to 1989.

This is a work in progress. I will be updating this document as I continue to transcribe talks and find additional references, and perhaps some day we might even have access to additional talks that we don’t have access to today. Nevertheless, after six or so years of slow but steady work on transcribing Katagiri Roshi’s talks, there is a solid basis to begin this project. 

All of the transcripts of Katagiri Roshi’s talks that I draw from (and more; with the exception of those on *The Song of the Jewel Mirror Awareness*) are on the  [Katagiri Transcripts](https://katagiritranscripts.net) website. If you are viewing this document as a PDF,  you should be able to follow the links to get to the complete transcripts. Katagiri Roshi’s dharma talks are being used with permission of [Minnesota Zen Meditation Center](https://www.mnzencenter.org/katagiri-project.html).

The purpose of the [Katagiri Transcripts](https://katagiritranscripts.net) project is to help convey the teachings of Katagiri Roshi and Eihei Dōgen to the next generation. I present this work in the spirit of ongoing investigation and practice. Any errors in understanding here are my own. 

## About the English Translations of *Fukanzazengi*

[SZ] indicates the [Sōtōshū translation of *Fukanzazengi*](https://www.sotozen.com/eng/zazen/advice/fukanzanzeng.html). This translation is commonly used in English-speaking Zen centers.

[EB] indicates text from the translation of *Fukanzazengi* by Norman Waddell and Masao Abe in *The Eastern Buddhist* magazine, Vol. 6, No. 2 (October, 1973), pp. 115-128. This is the translation that Katagiri Roshi himself was using in the 1970s.

[KR] indicates a translation which appears to be by Katagiri Roshi himself. 

```{=typst}
#pagebreak()
```

# Manuscript

```{=typst}
#v(2em, weak: true)
#figure(
  image("fukan-zazen-gi-rufu-bon-taisho.gif"),
  caption: [The _Rufu-bon_ ("Popular Version") of _Fukanzazengi_. The text is in Classical Chinese; the characters are read in vertical lines from right to left, with two blocks of text, top and bottom. Source: #link("https://en.wikipedia.org/wiki/Taishō_Tripiṭaka")[The Taishō Tripiṭaka], SAT Daizōkyō Text Database, Volume 82, #link("https://21dzk.l.u-tokyo.ac.jp/SAT/ddb-sat2.php?mode=detail&useid=2580_,82,0002&nonum=&kaeri=")[Text 2580]. Via #link("https://dharmawanderer.wordpress.com/2020/07/16/fukan-zazen-gi-original/")[dharmawanderer.wordpress.com].],
  gap: 1.5em
)
#pagebreak()
```

# Translation

> **Fukan Zazengi** (Universally Recommended Instructions for Zazen)
> 
> The way is originally perfect and all-pervading. How could it be contingent on practice and realization? The true vehicle is self-sufficient. What need is there for special effort? Indeed, the whole body is free from dust. Who could believe in a means to brush it clean? It is never apart from this very place; what is the use of traveling around to practice? 
> 
> And yet, if there is a hairsbreadth deviation, it is like the gap between heaven and earth. If the least like or dislike arises, the mind is lost in confusion. Suppose you are confident in your understanding and rich in enlightenment, gaining the wisdom that knows at a glance, attaining the Way and clarifying the mind, arousing an aspiration to reach for the heavens. You are playing in the entranceway, but you are still short of the vital path of emancipation.
> 
> Consider the Buddha: although he was wise at birth, the traces of his six years of upright sitting can yet be seen. As for Bodhidharma, although he had received the mind-seal, his nine years of facing a wall is celebrated still. If even the ancient sages were like this, how can we today dispense with wholehearted practice?
> 
> Therefore, put aside the intellectual practice of investigating words and chasing phrases, and learn to take the backward step that turns the light and shines it inward. Body and mind of themselves will drop away, and your original face will manifest. If you want to realize such, get to work on such right now.
> 
> For practicing Zen, a quiet room is suitable. Eat and drink moderately. Put aside all involvements and suspend all affairs. Do not think "good" or "bad." Do not judge true or false. Give up the operations of mind, intellect, and consciousness; stop measuring with thoughts, ideas, and views. Have no designs on becoming a buddha. How could that be limited to sitting or lying down?
> 
> At your sitting place, spread out a thick mat and put a cushion on it. Sit either in the full-lotus or half-lotus position. In the full-lotus position, first place your right foot on your left thigh, then your left foot on your right thigh. In the half-lotus, simply place your left foot on your right thigh. Tie your robes loosely and arrange them neatly. Then place your right hand on your left leg and your left hand on your right palm, thumb-tips lightly touching. Straighten your body and sit upright, leaning neither left nor right, neither forward nor backward. Align your ears with your shoulders and your nose with your navel. Rest the tip of your tongue against the front of the roof of your mouth, with teeth together and lips shut. Always keep your eyes open, and breathe softly through your nose.
> 
> Once you have adjusted your posture, take a breath and exhale fully, rock your body right and left, and settle into steady, immovable sitting. Think of not thinking, "Not thinking --what kind of thinking is that?" Nonthinking. This is the essential art of zazen.
> 
> The zazen I speak of is not meditation practice. It is simply the dharma gate of joyful ease, the practice realization of totally culminated enlightenment. It is the koan realized; traps and snares can never reach it. If you grasp the point, you are like a dragon gaining the water, like a tiger taking to the mountains. For you must know that the true dharma appears of itself, so that from the start dullness and distraction are struck aside.
> 
> When you arise from sitting, move slowly and quietly, calmly and deliberately. Do not rise suddenly or abruptly. In surveying the past, we find that transcendence of both mundane and sacred, and dying while either sitting or standing, have all depended entirely on the power of zazen.
> 
> In addition, triggering awakening with a finger, a banner, a needle, or a mallet, and effecting realization with a whisk, a fist, a staff, or a shout --these cannot be understood by discriminative thinking; much less can they be known through the practice of supernatural power. They must represent conduct beyond seeing and hearing. Are they not a standard prior to knowledge and views?
> 
> This being the case, intelligence or lack of it is not an issue; make no distinction between the dull and the sharp-witted. If you concentrate your effort single-mindedly, that in itself is wholeheartedly engaging the way. Practice-realization is naturally undefiled. Going forward is, after all, an everyday affair.
>
> In general, in our world and others, in both India and China, all equally hold the buddha-seal. While each lineage expresses its own style, they are all simply devoted to sitting, totally blocked in resolute stability. Although they say that there are ten thousand distinctions and a thousand variations, they just wholeheartedly engage the way in zazen. Why leave behind the seat in your own home to wander in vain through the dusty realms of other lands? If you make one misstep, you stumble past what is directly in front of you.
> 
> You have gained the pivotal opportunity of human form. Do not pass your days and nights in vain. You are taking care of the essential activity of the buddha-way. Who would take wasteful delight in the spark from a flintstone? Besides, form and substance are like the dew on the grass, the fortunes of life like a dart of lightning --emptied in an instant, vanished in a flash.
> 
> Please, honored followers of Zen, long accustomed to groping for the elephant, do not doubt the true dragon. Devote your energies to the way of direct pointing at the real. Revere the one who has gone beyond learning and is free from effort. Accord with the enlightenment of all the buddhas; succeed to the samadhi of all the ancestors. Continue to live in such a way, and you will be such a person. The treasure store will open of itself, and you may enjoy it freely.
>
> – Source: [sotozen.com](https://www.sotozen.com/eng/zazen/advice/fukanzanzeng.html)


```{=typst}
#pagebreak()
```


# Chapter 1: Universal Recommendation for Zazen

## Title

> 普勸坐禪儀  
> *Fukan zazen gi*

> Universally Recommended Instructions for Zazen [SZ]

> Universal Promotion of the Principles of Zazen [EB]

> Universal Recommendation for Zazen [KR]

## Commentary

Katagiri Roshi explains the term *zazen*:

> *Zazen* [is] Zen meditation: in Japanese *za zen* (坐禪). *Za* (坐) is “sitting.” *Zen* (禪) is zen, “tranquility.” 
>
> I always use the term *zazen*, because the zazen we do is a little different from the meditation that [...] other religions do. That’s why I want to use the original term *zazen*. 
>
> In Chinese, etymologically, the *za* [is that] two persons sit in the universe. (*Transcriber’s Note:* The character *za* 坐 depicts two people 人 sitting on the ground 土.) [...] That [indicates that] you have to sit with more than two beings, [and] not only human beings; you cannot sit alone. So you should sit with more than two beings on the earth, in the universe – not in your own egoistic, selfish territory. 
>
> [If] you must open yourself and sit in the universe, very naturally you have to sit *with* all sentient beings. That is called *sitting*. And then very naturally [...] *that* sitting is exactly *zen*, tranquility – because all sentient beings around you are exactly sitting with you! So very naturally that is called *zen*: tranquility. 
> 
> So you, and the universe, earth, all beings, and all circumstances, [...] become sitting with you, together. This is called *zazen*. All we have to do is to do our best to sit in the universe with all sentient beings. That’s *all* we have to do. 
>
> – From [“Katagiri Roshi’s Zazen Instruction” (1981)](https://katagiritranscripts.net/zazen-instruction). 

This was how Katagiri Roshi introduced *zazen* to a small group of people in 1981. Note that almost the very first thing he talks about is not a technical explanation, nor an individual goal, but that we sit with all beings, and not just human beings. 

This point will come up again, frequently. And we’ll return to the definition of zen as *tranquility* in Chapter 12: “Surrender to Tranquility.” 

Katagiri Roshi says about sitting down in *zazen*:

> *Anyone* can do it. Even if you are not Buddhist, or even if you cannot come [to the Zen Center], you can sit down. [...] This is *shikantaza* (wholehearted sitting). [...] This is *freedom* – open to *everybody*! No exceptions. 
>
> That’s why Dōgen Zenji says “Universal Recommendation for Zazen” – *universal* recommendation. It’s really *universal*. [It’s] not only weeding out on your own territory. Anyone can do it. Wherever you may be, you can do it. 
>
> – From [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 3,” June 11, 1979, at 1:02:07](https://katagiritranscripts.net/1979-06-11-Fukanzazengi-Talk-3#10207).

---

By “[it’s] not only weeding out on your own territory,” Katagiri Roshi means that this is not the kind of zazen where we are striving to attain liberation from this world, the practice of the *arhats* in early Buddhism:

> So by the practice of zazen, it’s possible to weed out even the seeds completely, and the weeds no longer grow. Some Buddhism says that means that if you attain enlightenment, which is the highest level of spiritual life, then at that time it’s not necessary to come back to the human world; you can stay constantly in heaven. *Arhats* and many saints in the history of Buddhism showed us [this], they experienced it. That’s why one of the four results of Buddhist practice, what the *arhat* does, is the highest spirit of spiritual life, which enables you never to come back to [being a] human being, the *samsaric* world. This is *arhat* practice. 
>
> This is also [a type of] zazen. You can do this. But that is just weeding out on their own territory; that’s all. And then, when they completely weed out on their territory – they don’t know what to do. So there is only death to wait for; that’s all. All they have to do is just to wait for their death. 
> 
> – From [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 3” (June 11, 1979) at 19:15](https://katagiritranscripts.net/1979-06-11-Fukanzazengi-Talk-3#1915).

So Katagiri Roshi says, this kind of zazen is not that. 

He adds:

> We can explain how important this kind of [Buddhist] practice is philosophically, psychologically – but it takes time. That is a huge world, the philosophical background, psychological background. But even though you don’t know [it], you can do it – right now, right here. This is a very urgent need; we have to do it. Whoever you are, wherever you may be, you can do it. 
>
> For instance, if you are in an office – well still you can do it. If there is no one there, you can sit down in a chair and calm yourself. If you are talking with somebody, you can realize a certain pause, where no words come up. For that time, you can return to yourself, and breathe. 
> 
> You can do it, okay? Wherever you may go. It’s really universal. It’s very simple. It’s *too* simple to realize. But, this is the best way. Not only for your life in *this* world, but in the next life, in the life after next life, after next next life, continually. 
> 
> – From [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 3” (June 11, 1979) at 1:09:51](https://katagiritranscripts.net/1979-06-11-Fukanzazengi-Talk-3#10951).

This is a small part of a much longer talk which ties together many ideas in *Fukanzazengi*, including this notion of practicing for lifetime after lifetime. We’ll return to those points in the following chapters.

But this is the conclusion: to do it.

```{=typst}
#pagebreak()
```

# Chapter 2: The Way

## Paragraph 1 Part 1

> 原夫道本圓通、  

> The Way is originally perfect and all-pervading. [SZ] 

> The Way is basically perfect and all-pervading. [EB] 
 
> The origin of the Way is perfect and all-pervading. [KR] 

## Commentary

According to *Kenzeiki*, a biography of Dōgen Zenji written in the 15th century, Dōgen’s deep question, the one driving him to seek out the truth of Buddhism, was something like this: “If, as the sutras teach, all people are endowed with Buddha-nature, why is it that we have to practice to realize that Buddha-nature?”

In the first part of *Fukanzazengi*, which we discuss in Chapters 2 through 8, Dōgen Zenji restates this question and answers it. To understand his answer, we first need to understand what Dōgen means by “the Way.”

“The Way” is *tao* or *dao* (道) in Chinese, or in Japanese, *dō*. Dōgen Zenji’s name, *Dō*-*gen* (道元), means “Way Origin.”

Katagiri Roshi gave a series of talks on Zen Master Dōgen’s *Gakudō-yōjinshū*, [“Points To Watch in Studying the Way”](https://katagiritranscripts.net/principles-of-practice). *Gakudō* means “study of the Way.” He explains the meaning of the character *dō*:

> *The Way* means the universal life beyond conscious or unconscious worlds. This is the Way, where all beings exist in peace and harmony, prior to the germination of any subtle ideas. [...] All sentient beings exist in the realm of the Way; that is called *universal life*. This life is open not only to human beings or living beings, but also inanimate beings: pebbles, water, et cetera. 
>
> – From [“Principles of Practice, Talk 1: The Purpose of Practice” (March 19, 1986)](https://katagiritranscripts.net/1986-03-19-Principles-of-Practice-Talk-1).

So here “the Way” is not a set of guidelines or procedures to follow, but *universal life*.  But what is *universal life*? And isn’t “the Way” the teachings of the Buddha – the *buddha-dharma* – which we need to follow?

We can say that to study the Way is to follow the teaching of Buddha. But we need to ask, what do we mean by “Buddha”? And also, what do we mean by “the teaching”?

---

Taking refuge in the Triple Treasure – *Buddha*, *dharma*, and *sangha* – is fundamental to all branches of Buddhism. In a Zen temple, we do this together at the start of every morning service, at the start of the Full Moon Precepts ceremony, and in many other ceremonies. We also take refuge in the Three Treasures in our daily life, keeping them close to our hearts.

In a typical translation, *Buddha* is understood as the historical Buddha or the religious personage of “the Buddha.” *Dharma* is often understood as “the teaching.” And *sangha* is usually understood as “the community.” But this misses the significance of these terms in Zen. According to Katagiri Roshi, *Buddha* is the universe. *Dharma* is the teaching of the universe. And *sangha* is the community that makes the universe and its teaching alive in their lives. 

Katagiri Roshi explains the Triple Treasure:

> Dōgen Zenji says:
> 
> > [Through] day and night, be mindful of the Triple Treasure. In your everyday life, be mindful of the Triple Treasure. 
> 
> Why? What is the reason why we have to do this? Dōgen Zenji says: 

> > We take refuge in the Buddha because he is our great teacher. 
>
> *Great* means completely beyond the human value good or bad. Buddha is *great* beyond human evaluation. The spirit, the essence of the universe, merit of the universe, and functioning of the universe is completely great, beyond your speculation. When you realize, you become the universe. *You become the universe* means, in other words we say Buddha. Shakyamuni Buddha – Gotama Siddhartha – realized the essence of the universe, the merit or virtue of the universe, [...] and functioning of the universe, then Gotama Siddartha [became] Buddha. 
>
>  > We take refuge in [the Dharma] because it is good medicine. 
> 
> *Dharma* is teaching; [the] teaching is completely beyond human evaluation, beyond the moral sense or ethical sense. The dharma is something coming from the truth, so it’s really beneficial to everyone, all sentient beings – just like a rain nurtures all kind of grasses, trees, pebbles, human beings, and the air, everything. That is dharma; that’s why dharma is good medicine. 
>
> – From [“Lay Ordination Lecture 3 of 7: Triple Treasure, Lecture 1” (March 8, 1986) at 14:00](https://katagiritranscripts.net/1986-03-08-Triple-Treasure-Lecture-1#1400).

In a different talk, Katagiri Roshi further explains the word *dharma*:

> *Dharma* is a very technical Buddhist term, and very popular. It’s a philosophical term, but it’s not philosophical, [it’s a] very spiritual term. So it’s a very complicated term. *At the least,* it has three meanings. If you use *dharma*, it is *the principle of existence*. And second, it is *phenomena*: *all* phenomena, visible and invisible. And also [it is] *teaching*. *Dharma* has at least those three meanings: *principle of existence*, and also *all phenomena*, and also *teaching*. Because you can experience it and you can teach it to people. This is our responsibility: we have to transmit this dharma to the next generation. So, we can teach. That is *dharma*. 
> 
> – From [“Verse of Opening the Sutra” (July 23, 1986) at 6:06](https://katagiritranscripts.net/1986-07-23-Verse-of-Opening-the-Sutra#606)

So *dharma* actually means at least three things: *the principle of existence*, *phenomena*, and *teaching*. And it’s implied that it means all three things at the same time.

Rounding out the Triple Treasure is *sangha*:

> [Dōgen Zenji says:]
> 
> > We take refuge in the Buddhist community because it is composed of excellent friends.
> 
> *Sangha* is a community, but it’s not the usual sense of community, because this community has lots of people who try to follow the Buddha’s way. [That’s why] they are excellent friends for you. 

After some explanation of the meaning of “excellent friends,” he continues:

> [...] This sangha is quite different from the usual sense of community. If people just gather and live together, it’s not *sangha*. Each of you has to be an *excellent friend* to others, because you must be following Buddha’s teaching. You must be following the essence of the universe, and the virtue of the universe, the functioning of the universe. And then you become excellent friends to others. 
> 
> – From [“Lay Ordination Lecture 3 of 7: Triple Treasure, Lecture 1” (March 8, 1986) at 14:00](https://katagiritranscripts.net/1986-03-08-Triple-Treasure-Lecture-1#1400).

This is more the sense in which we can say that the Way is the teaching of Buddha that we need to follow. The Way is the teaching of the universe, the *buddha-dharma*. And the community of people who are following the Way is the *sangha*.

--- 

And what is *taking refuge* in Buddha, dharma, and sangha? Katagiri Roshi says:

> If so, what is taking refuge? What is the point? How can we realize, how can we touch that spirit of taking refuge which turns into motive power? Here it says: 
>
> > The merit of having taken refuge in the Three Treasures inevitably appears when there is spiritual communion between the trainee and the Buddha. 
> 
> Here it says spiritual communion between the Buddha and the practitioner, the Buddha and you. “Spiritual communion” means interacting communion of appeal and response (*kannō-dōkō*).

So taking refuge in the the Triple Treasure is “interactive appeal and response with the universe” (*kannō-dōkō*). Katagiri Roshi says:

> In other words, if you try to reach out your hand to the universe, the universe reaches out its own hands. That is [spirituality, but in the] broad sense, it’s really true. And then Buddha, the spirit of the universe, and you – the path of your life and the path of the universe – become one, interconnected, crossing each other. 
> 
> That is called *dōkō*; the *dōkō* of *kannō-dōkō*. *Kan* means “appeal.” The *nō* of *kannō* is “response.” *Dō* of *dōkō* is “the path.” *Kō* of *dōkō* is “to cross.” So appeal and response come across, very quickly. 
> 
> When can you see this? That is exactly *shikan*, or *wholeheartedness*. 
> 
> – From [“Lay Ordination Lecture 3 of 7: Triple Treasure, Lecture 1” (March 8, 1986) at 33:20](https://katagiritranscripts.net/1986-03-08-Triple-Treasure-Lecture-1#3320).

*Shikan* (只管) here is the same word as in *shikantaza*, “wholehearted sitting.” This is the fundamental practice, here understood in the general sense that we can participate wholeheartedly in *any* activity.

Put another way, in taking refuge in dharma through the practice of *wholeheartedness*, we connect with the larger sense of ourselves which includes all things, all *phenomena*. Katagiri Roshi says:

> So if you practice like this, very naturally dharma is coming to your life, and your life manifests yourself as dharma. So very naturally your life [manifests] as *total personality*. 
>
> Do you know the [term] *total personality*? Total personality is your personality *including* trees’ life, others’ life, all beings. Your life is penetrating to the past, present, future, and also trees, birds... Japan, China, all of the world... pebbles, air... and then your personality becomes *whole*. This is *total personality*. 
>
> – From [“Depending on the Dharma” (August 3, 1988) at 11:30](https://katagiritranscripts.net/1988-08-03-Depending-on-the-Dharma#11:30).

*Total personality* is an important term that Katagiri Roshi uses frequently. In his talks on *Fukanzazengi*, Katagiri Roshi says that sitting down in zazen is about sitting down in the core of our total personality.

> ... let's sit down in the core of your total personality. That is *buddha-nature*. And then this total personality, which is called *buddha*, is completely perfect and all-pervading. Dōgen Zenji says, “The origin of the way is perfect and all-pervading.” 
>
> – From [“Fukanzazengi: Dōgen's Universal Recommendation for Zazen – Talk 1” (June 9, 1979) at 56:36](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1#5636).

So it seems *the Way* is *total personality*, which is our personality in connection with the whole universe of space and time. And this is *buddha-nature*.

> Bottomlessness of your personality is what is called *buddha*. We say *buddha*, or *vastness of your nature*, or *vastness of your capability*. [This is what] is called buddha-nature, or buddha, or buddha-dharma; we say so.
>
> – From [“*Blue Cliff Record* Case 52: Chao Chou Lets Asses Cross, Lets Horses Cross – Talk 1” (January 21, 1984) at 41:41](https://katagiritranscripts.net/1984-01-21-Blue-Cliff-Record-Case-52-Talk-1#4141).

--- 

But *total personality* is really not something abstract and separate from our day-to-day lives. In fact, Katagiri Roshi uses a term that might surprise people:

> I told you yesterday [about] the *whole personality* or *total personality*; the personality that, according to general Buddhism, is *buddha-nature*, or according Buddhist psychology it is called *karma*.
>
> That total personality has a double face. One face is [the] karma you have carried from the past. And the other face is [that] that total personality is completely beyond human criticism; that is really buddha-nature. You cannot know what karma is, because karma comes from the beginningless past, and is going to the endless future. That’s why in *Fukanzazengi* Dōgen Zenji says, “The origin of the way is perfect and all-pervading.”
>
> And then also, if you do zazen, the original face of existence appears, manifests itself. That is, as Dōgen says in *Fukanzazengi*, [perfect and all-pervading]: the origin of the way, the origin of existence, is perfect and all-pervading. That is *buddha-nature*. If you do zazen, immediately [it] appears. That is what is called the original nature of existence manifesting itself. So Dōgen says in *Fukanzazengi*.
>
> – From [“Fukanzazengi: Dōgen's Universal Recommendation for Zazen – Talk 2” (June 10, 1979) at 34:20](https://katagiritranscripts.net/1979-06-10-Fukanzazengi-Talk-2#3420).

So *total personality* is *buddha-nature*, but it is also *karma*: our ordinary, day-to-day lives, sometimes called “karmic life.” But our ordinary lives are not so ordinary.

Katagiri Roshi says that “total personality has a double face”: in terms of the Yogachara teaching of Mahayana Buddhism, that double face is called *ālāyavijñāna* and *tathāgatagarbha*. *Ālāyavijñāna* means “storehouse consciousness” or *karmic* consciousness. *Tathāgatagarbha* has the same meaning as *buddha-nature*. *Tathāgata* is another word for *buddha*, and *garbha* literally means “womb.” *Tathāgata* also implies “suchness”: it means something like “thus coming and going.” We could  think of *tathāgatagarbha* as “the origin of suchness.”

In Mahayana Buddhism *ālāyavijñāna* and *tathāgatagarbha* are two aspects of the same thing. According to Katagiri Roshi, they are like a piece of paper with two sides. Our practice in Zen is to deeply taste this *ālāyavijñāna* – that is, basically, *karma* – by being one with it. And in a sense, in that way we turn it over to see its other aspect: *tathāgatagarbha*, the world of Buddha. This world is totally free and all-inclusive: “perfect and all-pervading.” This is, as Katagiri Roshi says, “the origin of the Way.”

All this may seem complicated. The relationship between *ālāyavijñāna* and *tathāgatagarbha* is a basic and deep topic in Mahayana Buddhism which Katagiri Roshi discusses often, notably in his talks on [*Genjōkōan*](https://katagiritranscripts.net/genjokoan) and on [*The Awakening of Faith*](https://katagiritranscripts.net/awakening-of-faith). So why do we mention it? Because this is the same relationship we see in *Fukanzazengi.* “The origin of the Way is perfect and all-pervading” is *tathāgatagarbha*. The “flip side” that’s coming up is *ālāyavijñāna*. 

--- 

But practically, what does it mean to sit down and taste this *total personality* through *wholeheartedness*? Continuing his discussion of “interactive appeal and response with the universe” (*kannō-dōkō*), Katagiri Roshi says: 

> The *Saddharma Pundarika Sutra* (the *Lotus Sutra*) [talks about this]. If you read this just on the surface, it is kind of mysterious, but if you consider it deeply, it is very true. It says:
> 
> > The Buddha answered the Bodhisattva Infinite Thought: “Good son! If there be countless hundred thousand myriad *kotis* (a very large number) of living beings suffering from pain and distress who hear of this Bodhisattva Regarder of the Cries of the World, and with all their mind call upon his name, the Bodhisattva Regarder of the Cries of the World will instantly regard their cries, and all of them will be delivered.
> 
> That is really *faith*, total security. The moment your mind is vibrated, you cannot believe this. But right in the middle of *wholeheartedness*, you can believe it, beyond your senses, because [...] there is total realization of you, total presence of your life, which is exactly settling down right here, right now. That is called *wholeheartedness*. With wholeheartedness you call upon Avalokiteshvara. 
> 
> In other words, if you really see deeply the total picture of the human world, *samsara* – how transient the world is, how fragile human life is – then you can hear the cries. And then if you hear the cries, very naturally the cries of the human beings are simultaneously the listener, so-called Avalokiteshvara. So immediately you can appeal for help, and simultaneously the universe reaches out to you with its hands. [...] You can see the path through which you and the universe are crossing each other. 
> 
> And then how can you do this? That is by manifestation of your wholeheartedness. When you chant, when you repeat the name of Buddha, when you do *gassho*, you *do* it. And then, there is exactly the total presence of your life. That total presence of your life is exactly the same as the total presence of the universe, before you poke your head into it. And then you feel peaceful, simultaneously. 
> 
> That is sitting zazen, exactly. You don’t know; but even though you don’t know, if you sit exactly, totally, with wholeheartedness, some part of your body feels it. You can feel peaceful, because your presence and the presence of the universe are exactly crossing each other. 
> 
> – From [“Lay Ordination Lecture 3 of 7: Triple Treasure, Lecture 1” (March 8, 1986) at 33:20](https://katagiritranscripts.net/1986-03-08-Triple-Treasure-Lecture-1#3320).

It might seem surprising for Avalokiteshvara to appear in a discussion of Zen meditation, but this is common in Katagiri Roshi’s talks. Avalokiteshvara, The Bodhisattva Regarder of the Cries of the World, is deeply tuning in to the feeling of the universe, which is what we do in zazen. Avalokiteshvara represents *compassion* in Buddhism – or another word might be *empathy*. The core of Zen is both wisdom and compassion. 

If this seems religious, that’s because it is – but in a sense of the word that doesn’t involve dogmatism, or even theology. Katagiri Roshi often talks about religious practice, even “religious zazen,” but for him the word “religious” usually means something very close to “nondualistic.” In other words, “religious” here means basically the same as “wholehearted,” or *shikan* (只管). “Religious” zazen is “real” zazen – which means not clinging to ideas.

Yet we quickly get into discussions about whether Avalokiteshvara is real entity or not. Katagiri Roshi says:

> Who is Avalokiteshvara? *You*. Us. Exactly this body: *this is* Avalokiteshvara. 
> 
> Who creates this Avalokiteshvara? It doesn’t matter whether this Avalokiteshvara is a real, existing being or not. It doesn’t matter. This is [that] Avalokiteshvara is exactly you, all of you! 
> 
> – From [“*Kokyō*: The Ancient Mirror – Talk 2” (October 19, 1986) at 27:13](https://katagiritranscripts.net/1986-10-19-Kokyo-Talk-2#2713)

--- 

So to study the Way is to take refuge in Buddha, dharma, and sangha, and to turn karma into Buddha’s world. As we recite at the beginning of the Full Moon Precepts Ceremony:

> Taking refuge is to return home, arousing a fresh and vivid mind, openly and enthusiastically seeking for perfect peace. Even though body and mind are subject to birth, change and death, this moment of returning home offers the opportunity for the continuous practice of Buddha nature, the ripening of the sweet milk of the long river. 

This refers to the last line of Dōgen Zenji’s *Genjōkōan*:

> The wind of Buddhism makes manifest the great earth’s goldenness, and makes ripen the sweet milk of the long rivers.
  
“Making manifest the great earth’s goldenness” is our practice. “The long river” is our life: not just our limited, personal life, but all life, stretching from beginningless past to endless future.

We’ll return to this topic in the last chapter, where we discuss “the treasure store.”

```{=typst}
#pagebreak()
```

# Chapter 3: Practice-Realization

## Paragraph 1 Part 2

> 爭假修證。  

> How could it be contingent on practice and realization? [SZ] 

> How could it be contingent upon practice and realization? [EB] 

## Commentary

“Practice and realization” is a translation of the term *shushō* (修證). *Shushō* is also translated as hyphenated “practice-realization,” for reasons we will see in a moment. Or, some translators say “practice-enlightenment.” Understanding this term is essential for understanding Dōgen Zenji’s teaching, because essentially it *is* Dogen Zenji’s teaching.

The translation of *shu* (修) as “practice” seems straightforward, but the translation of *shō* (證) as “realization” is not. It is important not to assume what this “realization” means based only on the English word. Katagiri Roshi gave an entire talk on the subject of *shō*, which begins as follows:

> I would like to explain a little more about the [word] “realization” [that] Dōgen Zenji uses very often here: “practice and realization.” I don't know how you understand what *realization* is. I think this is my problem, how to translate this term in English. Well, English always uses “realization,” but I don't know *how* you understand this. 
>
> Dōgen uses three [words in Japanese meaning] “enlightenment.” One is *kaku* (覚): “awareness,” “awakening.” The second is *satori* (悟り, or 悟あ in Chinese): usually “enlightenment.” The third is *shō* (證). [...] *Literally* it means “verification” or “proof.” Literally, okay? This is also *shō*: [to certify], or to prove, or to verify, or to witness. So three terms are often used by Dōgen, but in this case, “realization” is corresponding to the third one – “proof” or “verification,” literally translated. But [...] I don't know what [English word] is best, so I have to explain a little bit about this one. 
>
> The first one and second one, *kaku* and *satori*, both are something which you can experience through the six senses. But *shō* translated as “realization” is a little more than that which you can experience or you can awaken [to]. [It has] a little deeper meaning than *kaku*, “awakening,” or *satori*, “enlightenment.”
>
> So I don't know how to translate it, but maybe we can say *shō*, translated literally as *verification* or *witness*, means “actualizing the consummation of being.” [Or actualizing the] ultimate nature of being. 
>
> “Consummation of being” – how can I say it – is a place where everything synchronizes with each other. Well, according to [what Buddha said], I think [whether] animate being or inanimate beings, all [were] simultaneously enlightened when he attained enlightenment. He said, “I and heaven and earth [...] are the same and one root, where all living beings attain enlightenment simultaneously.” That is a *consummation of being*. Consummation of the ultimate nature of being is the same and one place where everything coexists in peace. 
> 
> – From [“*Bendōwa*: Dōgen's Questions & Answers – Talk 5” (March 15, 1987)](https://katagiritranscripts.net/1987-03-15-Bendowa-Talk-5). 

Katagiri Roshi then explains that *shō* is the same as “suchness” or “thusness.” We’ll return to the topic of “suchness” in Chapter 11: “Practice Suchness Immediately.” He continues:

> So *shō*, the consummation of being, is not [something] you try to manifest. No, you cannot do it, because this is exactly the *ultimate* state of existence. You don't know [it]. But the unique way is to let it manifest by virtue of making your water clear or calm. Or, practically speaking, you really devote yourself to do something thoroughly, with sincere heart, *exactly* do it: then, the consummation of being comes out, emerges from [that] naturally. That is our practice. 
>
> – From [“*Bendōwa*: Dōgen's Questions & Answers – Talk 5” (March 15, 1987)](https://katagiritranscripts.net/1987-03-15-Bendowa-Talk-5). 

--- 

This is important, so here is another time Katagiri Roshi discussed *shō*, in one of his talks on the *Diamond Sutra*:

> In Japanese, “enlightenment” is described by three different characters. One is *kaku*: “awareness.” The second is *satori* – you are very familiar with this term, satori. The third is *shō*: that is usually translated as “realization.” 
> 
> Enlightenment, broadly speaking, is to know or to awaken to the real nature, the original nature of existence. The original nature of existence is *truth*. 
> 
> According to the first term, *kaku*, awareness, this kind of enlightenment is to know, to experience the truth at the conscious level. Still that experience of enlightenment which is called *awareness* is at the conscious level. So whoever you are, if you practice zazen – or even though you don’t practice zazen, if you do your best to take care of your life, living in peace with all sentient beings with your best effort – at that time everybody can experience awareness, which allows you to touch the core of existence. 
>
> This is the first experience. Everyone can do this. But this experience of awareness is still at the conscious level. So even though you understand the universe, there is still some difficulty for us to know how we should put it into practice. We don’t know what to do, because the experience of the universe through awareness doesn’t work [appropriately enough] in our daily living.
>
> The second is *satori*. Satori is a little deeper than the experience of awareness, because satori is that awareness which penetrates your body, your skin, muscle, bone, and marrow. You really understand what the universe is, how all beings exist, through your body and mind, skin, muscle, bone, and marrow. So your daily living is a little bit free from their difficulties, because you understand pretty well, and you know a little bit how to practice the universe in your daily living, how to practice the experience of satori in your daily living. In your daily living, maybe your attitude gradually becomes very gentle, compassionate to everybody. 
>
> But still this *satori* is not good enough, because it is still something which is going on at the conscious level. Sometimes you handle this satori at the conscious level, sometimes you can get out of the conscious level, but still, it goes back and forth, so it’s still very difficult for us to experience perfect stability in our daily living. 
>
> That is *satori*. Usually people understand Zen as cultivating the experience of satori; [they understand that] Zen practice gives us a chance to experience satori, and that is the final goal we are aiming at. But this is not the final goal, because the experience of satori is still tinged with something intellectual which is going on at the subconscious level. 
>
> The final goal is that you must be free from the experience of satori. That is the third, the one which is called *shō*, which literally means “verification.”
>
> Verification which is called *shō* is oneness with the original nature of being. There is no gap between; exactly your daily living is perfectly in accord with the original nature of existence, the rhythm of the nature of existence. 
>
> That is the third one, which is called *shō*, usually translated as “realization.” This third enlightenment is the highest spiritual level, in which you can be free from awareness and satori. There is no trace of satori, no trace of awareness. That is called “verification” because you are already one with the original nature of existence even if you don’t realize it. You are already right in the middle of the nature of existence. By this *shō* enlightenment your life is supported, helped constantly, regardless of whether you like or dislike it. That is the total picture of [the] existence you have. 
>
> This is enlightenment. That’s why Buddha says, “Is there any dharma which the Tathāgata has fully known as ‘the utmost, right and perfect enlightenment’?” This is really pointing to the third enlightenment, which is called *shō*: perfect, right, supreme enlightenment. But if you get *something* at the conscious level, it is not real enlightenment; it is called awareness, or satori, et cetera. Real enlightenment which is called *shō* is nothing you can get in your hand. But, you can *be with it*, always, constantly. 
>
> – From [“*Diamond Sutra*, Talk 9: Emptiness” (August 1, 1979)](https://katagiritranscripts.net/1979-08-01-Diamond-Sutra-Emptiness):

“Be with it” is the practice. Or sometimes Katagiri Roshi says “be right there,” or “right now, right here,” or “be right on.” We’ll discuss this more in the next section on the *dharma vehicle*.

--- 

Since the practice is “be right here,” practice is intimately connected with realization – in fact, they are one. The oneness of practice and realization is often presented as a key point of Dōgen’s teaching, if not his key point, period. A well-known statement from *Bendōwa* is:

> To think practice and realization are not one is a heretical view. In the buddha-dharma, practice and realization are identical.

About this, Katagiri Roshi says:

> So the points that Dōgen Zenji [makes] here: one point is that practice and realization must be one. And the second [point] is that practice and realization must go endlessly, and beginninglessly. [...] In other words, our practice must go forever.
>
> I think this is not Dōgen Zenji’s idea, this is the essential point of Buddha’s teaching. 
> 
> – From [“*Bendōwa*: Dōgen's Questions & Answers – Talk 4” (March 14, 1987)](https://katagiritranscripts.net/1987-03-14-Bendowa-Talk-4). 

“Practice and realization are identical” means there is no thing called “realization” that you (or anyone) can “have,” separate from ongoing practice. This is one reason why “practice and realization must go endlessly.”

“This is not Dōgen Zenji’s idea” means that fundamentally, Dōgen Zenji didn’t invent something new here. This is just Buddha’s teaching – both the teaching of the historical Buddha and the teaching of the universe. The expression may be refreshed, but the essential point is the same as it has ever been, or ever will be.

```{=typst}
#pagebreak()
```

# Chapter 4: The Dharma Vehicle

## Paragraph 1 Part 3

> 宗乘自在、何費功夫。  

> The true vehicle is self-sufficient. What need is there for special effort? [SZ] 
 
> The Dharma-vehicle is free and untrammeled. What need is there for one’s concentrated effort? [EB] 
 
> The dharma vehicle is free and unrestricted, why should we expend sustained effort? [KR] 

## Commentary

We’ve mentioned that the term *dharma* has at least three meanings simultaneously: *the principle of existence*, *phenomena*, and *teaching*. Katagiri Roshi also says:

> *Dharma* means that which is constantly supporting [or] upholding all beings, completely beyond human speculation. 
> 
> – From [“Verse of Opening the Sutra” (July 23, 1986) at 6:06](https://katagiritranscripts.net/1986-07-23-Verse-of-Opening-the-Sutra#606).

This relates to the meaning of *dharma vehicle*.

“Dharma vehicle” here is also translated as “true vehicle,” “fundamental vehicle,” “ancestral vehicle,” and in other ways, but the word “vehicle” (乘) appears in most translations. What do we mean by “vehicle”?

“Vehicle” is a common term in Buddhism: there is often discussion of “two vehicles,” “three vehicles,” “five vehicles,” and these vehicles perhaps represent different teachings or different schools of Buddhism. Dōgen Zenji mentions some of these vehicles in this passage in *Bendōwa*:

> You should also know that basically we lack nothing of highest enlightenment. Though we are forever endowed with it, since we are unable to be in complete accord with it, we have a way of giving rise to random intellections, and by chasing them as if they were real, we stumble vainly on the great Way. Because of these intellections, flowers in the air of various kinds appear: thoughts of a twelve linked chain of transmigration, or of realms of twenty-five forms of existence, views of three vehicles, five vehicles, Buddha, no-buddha – they are endless. You shouldn’t think that learning such intellectualizations is the right path of practice in the buddha-dharma. 
>
> But when you now totally cast aside all things and single-mindedly do zazen in accordance with the buddha-seal, then, beyond the realms of illusion and enlightenment, sentiments and calculations, untouched by the difference of unenlightened and enlightened, you immediately walk at ease beyond established forms and regulations and employ great enlightenment. What have those enmeshed in the traps and snares of words and letters to compare to this? 
>
> (From “Dōgen’s *Bendōwa*,” translation by Norman Waddell and Abe Masao in *The Eastern Buddhist*, Vol. IV, No. 1, May 1971, p. 124-157.)

Buddhism, particularly Zen or Mahayana Buddhism, seems rare among religions in the degree to which it is willing to throw its own teachings under a bus to try to point in the direction of real truth. (See, for example, *The Heart Sutra*.) 

But in these lines in *Fukanzazengi*, we don’t seem to be discussing “vehicles” in the sense of different teachings or practices. Here we are discussing the *one* vehicle – the *dharma* vehicle. 

--- 

Katagiri Roshi discusses these lines in his talks on *Blue Cliff Record* Case 2: “The Ultimate Path Is Without Difficulty,” talking about the *dharma vehicle* in connection with two other terms from the case: “the Ultimate Path” and “the fundamental vehicle of transcendence.” He says:

> In this pointer Engo Zen Master emphasizes the significance of “the task of the fundamental vehicle of transcendence.” In other words, that is the great path, or the Ultimate Path; he uses a different term [here], *the task of the fundamental vehicle of transcendence*. This is the main point in this pointer. Plainly speaking, this is the truth, or original nature of existence, or *dharma*. Dōgen Zenji said in *Fukanzazengi*, “The dharma vehicle is free and unrestricted, why should we expend sustained effort?” So Dōgen uses the term *dharma vehicle*. 
> 
> – From [“*Blue Cliff Record* Case 2: The Ultimate Path Is Without Difficulty, Talk 1” (January 19, 1980)](https://katagiritranscripts.net/1980-01-19-Blue-Cliff-Record-Case-2-Talk-1).

Katagiri Roshi spends much of Talk 1 unpacking this; it’s well worth reading, but a bit too much to include here. In Talk 2 he sums it up:  

> Yesterday I told you, the “Ultimate Path” is the same as “the task of the fundamental vehicle of transcendence.” Usually truth is regarded as something which exists far from us, which no one can touch, but I don’t think Buddhism understands it in that way. The truth is always with us. So the characteristic of truth is completely something *transcendent*, which means beyond human speculation – good or bad, right or wrong. It makes all beings live in peace and harmony. That is characteristic of the truth or universe: unifying all things, beyond human judgement, good or bad, right or wrong. 
>
> So from this point, how can we approach truth, how can we reach this truth? That’s why we have to manifest ourselves in the state of transcendence. “Transcendence” means the state of a person who is never tossed away by judgement, good or bad, right or wrong. 
> 
> That’s why in zazen we shouldn’t judge ourselves, good or bad, right or wrong. Anyway right now, right here, all you have to do is to let the flower of your life force bloom. At that time, good or bad, right or wrong appears and disappears very naturally. But … if you meddle with those thoughts, judgements, evaluations, [then] simultaneously the many kinds of [affective preferences] appears. That is a problem for us, which leaves human beings in confusion and bewilderment.
> 
> So in order to be one with the truth, we have to manifest ourselves in the state of a person who is never tossed away by thoughts and ideas. That means, yesterday I told you, under all circumstances we have to release and forget ourselves, and throw ourselves away to zazen when you have to do zazen. When we have to do gassho, we have to *do* that. At that time, you can really manifest yourself: bloom the flower of life force from moment to moment. Wherever you may be, it is just like a lotus flower.
> 
> That is “the task of the fundamental vehicle of transcendence,” which is called the Ultimate Path. That is really the great vehicle which you are right on. Truth is not something which we can think, we can envision, we can believe, but it is something that you have to *be right on*. That is the Ultimate Path. At that time, it is without difficulty. It’s really just to be right on the vehicle, which is absolutely transcendent of human evaluation.
> 
> – From [“*Blue Cliff Record* Case 2: The Ultimate Path Is Without Difficulty, Talk 2” (January 20, 1980)](https://katagiritranscripts.net/1980-01-20-Blue-Cliff-Record-Case-2-Talk-2).

Normally when we hear the word “transcendence” we might think it means going beyond daily life, but in a sense this is the opposite. This transcendence is not about transcending reality, it’s about transcending our evaluations of it. It means not being stuck, just being *right on* daily life – right on the vehicle. 

---

“Vehicle” implies that, at least when you get on it, you’ll be taking a ride. So at that point, “what need is there for one’s concentrated effort?” Katagiri Roshi discusses this later in Talk 1:

> Zen is sometimes misunderstood by people because we don’t have a particular object which is called a divine entity, which is called God, which is called the soul, or whatever you say. [...] So very naturally, in the Buddhistic world it might be easier for us to lose what is called *faith*, if you like. *[He chuckles.]* We use the term *faith* and *Buddhist faith*, et cetera. It’s pretty easy [to lose faith], because there is nothing to depend on. 
>
> We *want* [something]. But usually if you see something you want to depend on objectively, that is something different from your daily life – because we always have to research what it is. Buddha or Avalokiteshvara, whatever it is: you very naturally want to research what it is. That is ontology, philosophy, psychology. “What is it?” Always the question comes up. And that question really prevents you from releasing and forgetting yourself and throwing yourself into Buddha’s home. 
> 
> [The question] is important, but you cannot be *obsessed* with it. That’s why Buddhas and ancestors constantly say, “Get one hundred percent.” If you want to perform gymnastics, get one hundred percent. How? Right now, right here, what should you do? Jump in. This is very practical... because it is not the ontological object, it is something [where] you have to communicate very closely with your daily life. For this, what should you do? Jump into it. Throw yourself into Buddha’s home. 
> 
> Without this, it’s very difficult. Particularly when you do zazen, this is the very fundamental practice for us, that’s why we have to throw [ourselves] into zazen itself. If you always create some delusion or fascination within your mind, it is not perfect zazen. I always tell you, zazen must be *pure* zazen. You have to get one hundred percent. We have to grab zazen perfectly. If you can’t, that is zero, completely zero. No ninety-nine percent. We don’t believe this, but this is a very fundamental, important practice for us. Only when you throw yourself into zazen, at that time, what is called zazen blooms. That is what is called Buddha, Buddha’s home. 
> 
> But if you believe zazen is like this, well, you believe zazen is a particular practice. So Zen says zazen is *not* a particular practice; your daily life is practice. *Gassho*, working, having breakfast – we have to get one hundred percent. We should handle our daily life with wholeheartedness. This is what is called *shikan*.
> 
> At that time, your daily life becomes *vehicle*. What you call the task is “the task of the fundamental *vehicle* of transcendence.” *Transcendence* means completely there is no need for your effort; function comes from Buddha’s world. Something takes care of you, if you do it. If you create your circumstances which are called perfect zazen, then perfect zazen takes care of you – even though you don’t want it. 
> 
> If you always see the zazen from your viewpoint, always there is a question. There is nothing to get, so that’s why you are very skeptical: “Should I spend my whole life doing zazen which is useless? Nothing to get, nothing to develop?” Ridiculous. You cannot do this. But even though you don’t know how much your life or your personality develops or not, well, if someone [has open eyes, they] know pretty well how much you have been developing. 
> 
> Anyway, at that time (when your daily life becomes *vehicle*), there is no need for your particular, sustained effort. Why should we expend sustained effort? All you have to do is throw yourself into zazen. At that time, something helps you. That something is completely transcendent. Nothing to say. Nothing to do. 
> 
> That’s why that is “the task of the fundamental vehicle of transcendence.” All you have to do is constantly you should be right on this vehicle, one hundred percent. That is really vast. Nothing holy or not holy, and nothing good or bad. All you have to do is just get the bar, with wholeheartedness. 
> 
> – From [“*Blue Cliff Record* Case 2: The Ultimate Path Is Without Difficulty, Talk 1” (January 19, 1980)](https://katagiritranscripts.net/1980-01-19-Blue-Cliff-Record-Case-2-Talk-1).

It may sound intimidating to have to get one hundred percent, but it isn’t a test, it’s an opportunity. Every moment is an opportunity to be on the vehicle. 

--- 

We mentioned earlier that another term for “the fundamental vehicle” is “the great path.” Dōgen Zenji says that the great path is “transcendence” or “going beyond” but it also is “complete actualization.” Katagiri Roshi explains:

> Dōgen Zenji [says this] very simply in *Zenki*, “The Whole Works.” It’s very beautiful words. [...] 
> 
>> The great path of the buddhas in its consummation is passage to freedom, is actualization. 
> 
> “In its consummation” means in its ultimate nature. If you see it in terms of ultimate nature of being, at that time there are two meanings of “the great path of the buddhas.” One is “passage to freedom” – that means *emancipation*. Always something goes beyond; goes beyond the framework of the table, or tape recorder, or Katagiri, or floor and lights, everything. Completely beyond. And [second,] it is also “actualization.” We call [that] *genjō*. *Genjō* means complete actualization, complete manifestation. *Gen* means “manifestation,” *jō* means “completion” or “achievement”...  well, “completion” is better. So, “complete actualization.”

This term *actualization* came up in the previous chapter, where Katagiri Roshi discussed the term *shō* or “realization” as “actualizing the consummation of being” or “actualizing the ultimate nature of being.” What do we mean by “actualization”? He continues:

> So showing your form called *gassho* is something *actualized*. But something actualized by you is not something you can see with your six senses – because it is a perfect actualization, beyond good or bad, right or wrong. Why? Because its nature is based on *emancipation*, the functioning of emancipation – *freedom*. The functioning of the passage to freedom. 
> 
> That’s why next Dōgen Zenji [says], 
> 
> > That passage to freedom in one sense is that life passes through life to freedom. 
> 
> If you see life, immediately we can see life in terms of dualism. At that time, [there are] life and death. The same applies to death. This is natural; but the real picture of life is not something like this. That’s why we have to see the real picture of life! Otherwise, it’s very difficult to build up peaceful life, day to day. That’s why ancestors and buddhas are always talking about this. Even though it is difficult for us, we have to think [about it], consider [it] deeply. 
> 
> And also he explained,
> 
> > When that actualization is taking place, it is without exception the complete actualization of life. 
> 
> So the life you can see is not life opposed to death, or [life that] you handle by your feeling – good or bad, right or wrong, dislike or like. The life you can see is complete actualization. This is the form of life, feeling of life you can see, you can hear. So what is life? Life is something more than you can think. 
> 
> And also he said,
> 
> > It is the complete actualization of death. 
> 
> That means when that actualization is taking place, it is complete actualization of death. So death is what? Death is something more than you can think, opposed to life. If you deal with death opposed to life, it scares you. But death is what? Death is complete actualization beyond like or dislike, or good or bad, right or wrong, hatred or not-hatred. Completely beyond, because it is based on the functioning of freedom – passage to freedom. 
> 
> So life passes through life to freedom, and death passes through death to freedom. Table passes through the table to freedom! This is perfect, complete actualization. This is a *form*. That’s why form is important. 
> 
> For instance, Ryokan Zen Master in Japan, who is pretty well known by Zen students. He looked like a shabby monk, not a usual monk. He didn’t have a temple; he stayed in a very tiny hut, and he lived by begging. [It is an] interesting story around him. And right before he was going to die, he was asked by his disciples: “What do you think about life?” And he said: “A maple leaf is falling, showing its front and back.” 
> 
> This is life, for him. You can understand it, you know? What is life? Life is just like a maple leaf is falling. “Falling” means your life is marching toward death. *[He chuckles.]* Marching to the graveyard. And on the way to the grave, what happens? Showing your back, showing your front – that’s it. Showing crying, showing pleasure – showing suffering, always. This is life. 
> 
> Somebody asked me to write a calligraphy, so I added one more thing: death. And about death I said, “When [fall of the maple leaf] is taking place, it is no failure [to] fall.” Do you understand? It is no failure in [falling]. In other words, right in the midst of falling, there is no failure.
> 
> “No failure” means completely beyond success and failure: just going. *[He laughs.]* No way. This is life; this is death. Because death is completely beyond. 
> 
> And also, “completely beyond” is not abstract; it is completely something *actualized*, which is complete and perfect. That’s why the scenery of Fall is beautiful. It’s very beautiful. Sometimes it makes me pensive or sad, and feeling human impermanence. But as a whole, autumn is autumn. Through the fall of a single leaf, you can realize the whole world becomes autumn. So that’s why the fall of a leaf is something more than the fall of a leaf – it’s the total picture of autumn.
> 
> Is the total picture of autumn something abstract for us? No. The single maple leaf shows it exactly. 
> 
> That is our life. [This is] Katagiri’s life right now – next moment, I don’t know if my life is going on or not. Right now, all I can do is just sit down and talk about Buddha’s teaching, anyway. That’s it. Beyond good or bad, right or wrong, or like or dislike. 
> 
> That is what Dōgen Zenji says (in *Zenki*, “The Whole Works”). It is a very beautiful first and second paragraph, talking about exactly the total picture of the human world. 
> 
> – From [“*Blue Cliff Record* Case 87: Medicine and Disease Subdue Each Other – Talk 2” (October 16, 1988) at 20:40](https://katagiritranscripts.net/1988-10-16-Blue-Cliff-Record-Case-87-Talk-2#2040)

--- 

We’ve mentioned Mahayana Buddhism, of which Zen is a part. It’s well-known that Mahayana means “Great Vehicle.” What is perhaps less well understood is that this term is pointing not so much at the greatness of a doctrine of Buddhism, but rather at the greatness of reality. Katagiri Roshi talks about this in the introduction to his series of talks on *The Awakening of Mahayana Faith*, a foundational text of Mahayana Buddhism:

> [In the word] *mahayana*, *maha* is “great,” *yana* is “vehicle.” In this book, *mahayana* is described [as] the essense of what is now, here, or the ultimate nature of what is here and now. Two meanings: one is what is the ultimate nature of what is here and now, and also the second meaning is “embracing.” So *maha* means the essence or ultimate nature of what is here, now, [and] that *maha* is to embrace all sentient beings. That is the meaning of *maha*. 
>
> And the function of the *maha* is a kind of vehicle to carry all sentient beings; that’s why we say “vehicle.” So *Maha-yana*; *yana* means “vehicle.” All sentient beings are carried on [it]. That is *mahayana*. 
> 
> [...] I have to say more [on] Mahayana *faith*, [as in] *Awakening of Faith*. This book is [a] teaching of Buddhist faith: not the usual Hinayana Buddhist faith, but Mahayana Buddhist faith. 
> 
> Mahayana is kind of the essense of the Buddhist faith, or [the] object of faith we believe in. Mahayana is the object of faith because *maha* means *essense of being* or ultimate nature of what is here and now, so that is really the object of our faith. But it is very pure, because the *maha* is the essense of being which embraces all sentient beings and carries them. So it is very pure function. That’s why the object of faith is something very pure, beyond human control, human speculation. Completely pure and clean. 
> 
> – From [“*The Awakening of Faith* – Talk 1: Introduction and Invocation” (March 16, 1984)](https://katagiritranscripts.net/1984-03-16-Awakening-of-Faith-Talk-1).

The term *Hinayana* is now considered pejorative and we avoid using it. Humans being humans, in history the terms *Mahayana* and *Hinayana* were immediately assigned to groups of people, but we should consider that this is not the deeper meaning of these words. As we shall see in the next chapter, we might even think of these as two aspects of practice that work together. 

```{=typst}
#pagebreak()
```

# Chapter 5: Free from Dust

## Paragraph 1 Part 4

> 況乎全體逈出塵埃兮、孰信拂拭之手段。大都不離當處兮、豈用修行之脚頭者乎。  

> Indeed, the whole body is free from dust. Who could believe in a means to brush it clean? It is never apart from this very place; what is the use of traveling around to practice? [SZ] 
 
> Indeed, the Whole Body is far beyond the world’s dust. Who could believe in a means to brush it clean? It is never apart from one right where one is. What is the use of going off here and there to practice? [EB] 

## Commentary

“The whole body” is *zenshin* (全身) in Japanese. *Zenshin* as “the whole body” also appears in Dōgen’s *Ikka myōju*, “One Bright Pearl”:

 > Thus, the suchness and beginninglessness of this bright pearl is limitless. It is the one bright pearl of all the worlds in the ten directions; it is not described as “two” or “three.” Its whole body is a single true dharma eye; its whole body is the true body; its whole body is a single phrase; its whole body is radiance; its whole body is the whole mind. When it is the whole body, it is not obstructed by the whole body. It is round, round; it rolls round and round.
>
> – From *Treasury of the True Dharma Eye: Dōgen’s Shōbōgenzō, Volume I-VII*, by the Sōtō Zen Text Project, p. 225.

So perhaps we could say that “the whole body” means your personal body and mind, but also the entire universe in space and time. 

Consider this verse, which is probably the source of the common Zen expression “stepping off the top of a hundred-foot pole” which is used by Dōgen:
```{=typst}
#pagebreak()
```
> 百丈竿頭不動人、雖然得入未為眞。百丈竿頭須進歩、十方世界是全身。  
> 
> The person unmoving atop a thousand-foot pole —  
> Even though they’ve entered, it’s not yet the real thing.  
> They should step off the top of the thousand-foot pole;  
> The worlds in the ten directions are their entire body.  
> 
> – Verse by Changsha Jingcen (長沙景岑) (dates unknown). From *Treasury of the True Dharma Eye: Dōgen’s Shōbōgenzō, Volume I-VII*, by the Sōtō Zen Text Project, p. 321.

“Entire body” here is *zenshin*. So there is a sense of stepping into this vastness which contains everything... or rather, which *is* everything.

We’ll come back to this poem in a moment.

---

What is this “dust” that the whole body is free from? Briefly, we could say *delusion*: delusion about our karmic life. 

This gets us back into our discussion of *karma*, and the fundamental teaching that *karmic life* is not separate from the *total dynamic working* of the whole universe. Katagiri Roshi mentions this “dust” while speaking about the need to “just be there,” in other words just be present in buddha-nature:

> ... This is total dynamic working. You become exactly one.
>
> That [is what Dōgen Zenji talks about] in the chapter “Buddha Nature.” The terms here are a little bit difficult, but let me read it:
> 
> > Therefore the self and environment of sentient being, whole being is not in the least involved in the waxing influences of karma, ...
> 
> This is the usual worldly affairs, our karmic life. 
> 
> >  ... is not bred by illusory causations, does not come into being naturally, is not practiced or realized through miraculous powers. Were sentient beings, whole being contingent on the power of karma or on causes or on coming into being naturally, then the realization of all saints and the enlightenment of all Buddhas and the eye pupils of buddhas and patriarchs also will be produced in these ways, and they are not. The entire world is completely free of all dusts as object to the self. Right here there is no second person.
> 
> “Right here there is no second person”: [that is,] karmic life. How can you be free from karmic life? By realization of the karmic life, you can be free from karmic life. 
> 
>But what do we mean, “realization of karmic life?” That is still vibration of the mind (i.e., a subtle form of thinking). You have to understand what is karmic life. [*Real*] karmic life is not the karmic life separate from this one world, Buddha’s world. But if you say “by realization of the karmic life *I* will be free from karmic life,” this is already you believe that karmic life is separate! So that’s why here it says [that] karmic life is exactly Buddha’s world, all sentient [beings,] whole being. That means the whole universe. 
> 
> If so, do we believe [there is] no karmic life? Yes [there] is; here is karmic life! Because it is very closely connected with the one world, so-called *whole being*; that’s why it exists. 
>
> If so, can we not be free from it? But you can be free from it, because [...] “free from” means [there is] no karmic life, because it is exactly connected with the one world, so-called whole universe. That means the karmic life is exactly the whole world by itself – not karmic life *is* the whole world, karmic life *exactly whole world*, no partition between. This is the reality of karmic life, the reality of the samsaric world, which is constantly going...
>
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986) at 15:16](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4#1516)

That, in brief, is why “the entire world is free from dust.” Yet we do not deny the conventional reality: “Hey, look! Dust!” Yet the entire world is *free* from it. 

That is basically the dynamic of what follows in this chapter... with some exciting historical drama thrown into the mix.

--- 

“Who could believe in a means to brush it clean” is a reference to [*The Platform Sutra*](https://katagiritranscripts.net/platform-sutra) and the well-known story of the Sixth Ancestor, which is considered a foundational story in Chinese Buddhism. 

In the story, the Fifth Ancestor, Great Master Hung Jen, challenges his monks to “use the wisdom-nature of your own original mind to compose a verse”; the monk who understands and expresses the great meaning will become his successor. The top student Shen Hsiu (Japanese: Jinshū) writes a verse comparing Buddhist practice to brushing dust from a mirror to keep it clean. The underdog student Hui Neng (Japanese: Daikan Enō) composes a responding verse, and becomes the Sixth Ancestor.

So although the word “mirror” does not appear in *Fukanzazengi*,  “mirror” is implied by “brushing it clean.” But *Fukanzazengi* says “the whole body” is far beyond the world’s dust. How is “the whole body” related to the mirror? 

The mirror is a common image in Zen Buddhist literature, and it is a deep subject, a bit challenging. Very briefly, we might say that the mirror is the absolute truth which is like a spacious sky, and also it is that which reflects all things, all phenomena, all *dharmas*. So perhaps we can say that the mirror reflects the whole body; the whole body is the reflection of the mirror. This experience “is never apart from one right where one is.”

For a deeper dive into the meaning of *mirror* in Zen, see Katagiri Roshi’s commentary on Dōgen's Zenji’s [“*Kokyō*: The Ancient Mirror”](https://katagiritranscripts.net/kokyo). Katagiri Roshi also talked about zazen being like a mirror in [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 5” (June 13, 1979)](https://katagiritranscripts.net/1979-06-13-Fukanzazengi-Talk-5#1234).

--- 

Returning to *The Platform Sutra* and “brushing it clean”: Katagiri Roshi tells the whole story with commentary, but let’s just look at what he says about the verses:

> [Shen Hsiu’s] poem is pretty well-known by everyone as one of the Zen stories:
>
>> The body is a Bodhi tree,  
>> The mind like a bright mirror stand.  
>> Time and again brush it clean,  
>> And let no dust alight.  
> 
> And also later Hui Neng wrote his poem. His poem is: 
>
>> Originally Bodhi has no tree,  
>> The bright mirror has no stand.  
>> Originally there is not a single thing:  
>> Where can dust alight?  
>
>Sometimes people deal with the two poems separately, and evaluate which is right, which is wrong, but I don’t think that is the right understanding. Both poems work together in our practice. I think you cannot separate them.
>
> So, according to Shen Hsiu, I think he stands always in the dualistic world, looking at himself and [trying] to reach the buddha-nature. From this point, “the body is a Bodhi tree”: we are buddha-nature but we are not buddha-nature, so we have to realize, we have to see into our own nature. [...] “The mind like a bright mirror stand”: this is exactly the same as the teaching of nirvana. So, we are Buddha. “Time and again brush it clean”: but we are living in the human world, so it’s easy for us to get “dusty”; that’s why we have to always brush it clean. “And let no dust alight.” So, constantly practice. 
> 
> This is one aspect of the practice: seeking for the truth, constantly, from the beginning to end. Even if you attain enlightenment, even if you become buddha, constantly we have to seek. 
> 
> And on the other hand, the other aspect of practice is to descend to the human world to share your life with all sentient beings. [This is the spirit of Hui Neng’s poem.] “Originally Bodhi has no tree, the bright mirror has no stand”: because our foundation is already buddha-nature, so there is no particular thing to discuss or to forget. So constantly we have to stand up there, and then we can deal with the human world. “Originally there is not a single thing: where can dust alight?” So, we have to descend to the human world and save all sentient beings. 
> 
> – From  [“*Platform Sutra* – Talk 1” (March 6, 1987) at 47:57](https://katagiritranscripts.net/1987-03-06-Platform-Sutra-Talk-1#4757). 

If “originally there is not a single thing,” why does that mean that we have to “descend to the human world and save all sentient beings”? Here let’s return to the poem we quoted at the beginning of the chapter:

> The person unmoving atop a thousand-foot pole —  
> Even though they’ve entered, it’s not yet the real thing.  
> They should step off the top of the thousand-foot pole;  
> The worlds in the ten directions are their entire body.  

We could say that the first part of the poem, “standing unmoving atop a thousand foot pole,” is realization that “there is not a single thing” – that is, realization of “emptiness.” That’s hard practice! Even if we wanted to, we could not stay there – because “emptiness” is not really “nothingness,” it’s “everythingness.” So rather than keep “ascending” to a pure practice, we need to come down. That’s where we realize that we share our lives with all beings.

And yet, we need to climb that thousand-foot pole. This matter of both Shen Hsiu’s and Hui Neng’s practices working together is revisited during the questions and answers:

> **Question:** Hojo-san? If Shen Hsiu’s poem speaks to one aspect of our life reality, and Hui Neng’s poem speaks to another aspect, is real reality beyond both of them? 
> 
> **Katagiri Roshi:** Yes. And they work together. 
> 
> – From  [“*Platform Sutra* – Talk 1” (March 6, 1987) at 1:02:08](https://katagiritranscripts.net/1987-03-06-Platform-Sutra-Talk-1#10208). 

So although the line “who could believe in a means to brush it clean” might initially seem to be supporting the verse attributed to the Sixth Ancestor Hui Neng over the verse attributed to Shen Hsiu, keep in mind that the next words in *Fukanzazengi* are, “and yet.” As Katagiri Roshi states above and on other occasions, these perspectives are two aspects of the same reality, and they work together. They are two sides of the same coin, and Dōgen’s “and yet” is basically flipping the coin. 

---

Yet, in large part due to the *Platform Sutra*, it is commonly understood that there was a “Northern School” and a “Southern School” in early Zen, and that the Northern School represented “gradual enlightenment,” while the new Southern School represented “sudden enlightenment,” and the Southern School is regarded as superior. 

That is the story that we often hear. However, this does not exactly seem to be Dōgen Zenji’s understanding, nor Katagiri Roshi’s. 

Katagiri Roshi even notes that Dōgen Zenji refers to the *Platform Sutra* as “a forged writing.” According to Dōgen:

> The essence of *Buddhadharma* has never been to see into one’s own nature. Which of the seven past Buddhas or twenty-eight Indian patriarchs ever said that Buddhadharma consisted merely of seeing into one’s own nature? It is true that the sixth patriarch spoke about this question in the *Platform Sutra*, but as this is a forged writing, it cannot be said to represent his true teachings, or to have the transmission of the dharma. We descendents of the Buddha shouldn’t rely on it. 
>
> – From *Zen Master Dōgen: An Introduction with Selected Writings*, Chapter 10: “A Monk at the Fourth Stage of Meditation (*Shi-zen Biku*)”, by Yuho Yokoi with Daizen Victoria. This is quoted in [“*Platform Sutra* – Talk 1”](https://katagiritranscripts.net/1987-03-06-Platform-Sutra-Talk-1).

First, an explanation: “to see into one’s own nature” is *kenshō* (見性), a term that many Zen students will be familiar with. *Kenshō* is usually understood as “an enlightenment experience,” which isn’t necessarily wrong. Two points here: *kenshō* (見性) is not the same as *shō* (證) or “realization,” which we discussed in Chapter 3: “Practice-Realization.” Instead, *kenshō* is considered to be basically the same as *satori*. 

And there is a sort of controversy about this, in that the *Platform Sutra* more or less says that *kenshō* is the point of Buddhist practice, while Dōgen more or less says that that’s ridiculous, as above. This is discussed at length in [“*Platform Sutra* – Talk 1,”](https://katagiritranscripts.net/1987-03-06-Platform-Sutra-Talk-1) and the matter is probably relevant, since *kenshō* is sometimes associated with “sudden enlightenment.” However, it need not concern us too much at the moment. Just remember that often when Katagiri Roshi mentions *satori*, he could equally be referring to *kenshō*.

But back to the forgery. Katagiri Roshi answers a question about this:

> **Question:** So, Dōgen considered this a forgery?
> 
> **Katagiri Roshi:** Uh, not only Dōgen. I think the introduction written by Echū, who was one of Hui Neng’s disciples, [talks about this]. Originally the *Platform Sutra* [was] written by one of the Sixth Patriarch’s disciples, but he didn’t publish it, and then other monks, other disciples, always carried it, and passages which [the] other disciples had [directly heard of] the Sixth Patriarch’s teaching were added to this original version. That’s why [it’s] “mixed up.”
> 
> That is the general understanding, in Japan, in China, about this. So it’s not *exactly* the Sixth Patriarch’s teaching. We are disappointed if we [hear] that, but still we use this Sixth Patriarch’s *Platform Sutra* as one of the Zen Buddhist textbooks. 
> 
> So that’s why Dōgen Zenji criticizes [it]... [Although] criticism is [not the right word]. Dōgen Zenji tries to let us know what the *real* teaching of the Sixth Patriarch is, instead of putting it down. 
>
> – From [“*Platform Sutra* – Talk 1” (March 6, 1987) at 54:25](https://katagiritranscripts.net/1987-03-06-Platform-Sutra-Talk-1#5425). 

It’s not clear what introduction Katagiri Roshi is referring to above, but “Echū” probably refers to National Teacher Dazheng, Nanyang Huizhong (675-775 CE), an important disciple of the Sixth Ancestor who often appears in kōans and is the source of several literary phrases used by Dōgen. In *Sokushin Zebutsu* (“This Mind Itself Is Buddha”), Dōgen approvingly quotes National Teacher Dazheng as he, among other things, criticizes “folk stories” or “vulgar tales” added to *The Platform Sutra* that “erase” the true meaning of the Sixth Ancestor’s teaching:

> “When I was wandering about some time ago, I often encountered this type. These days, they’re particularly flourishing. They gather assemblies of three to five hundred and, gazing up at the Milky Way, tell them, ‘This is the message of the South.’ They
revise the *Platform Sutra*, mixing in vulgar tales and erasing the sage’s intent, misguiding and confusing later followers. How could it represent the oral instruction? How painful that our tradition is so ruined!”
>
> – From *Treasury of the True Dharma Eye: Dōgen’s Shōbōgenzō, Volume I-VII*, by the Sōtō Zen Text Project, p. 156.

It seems that at least in some circles, it has always been understood that the *Platform Sutra* contains revisions by more than one person, some of which are problematic.

--- 

Western historical scholarship may be catching on to this point of view. John R. McRae’s *The Northern School and the Formation of Early Ch’an Buddhism* provides a compelling look at the history behind the composition of the *Platform Sutra*. The introduction to McRae’s posthumously released *Zen Evangelist: Shenhui, Sudden Enlightenment, and the Southern School of Chan Buddhism* sums up the general point: 

> McRae's meticulous analysis of the Northern school materials reveals the distortions and biases of the received tradition. To pick a single example, McRae takes to task the standard narrative that Northern teachers advocated a gradual path—that they viewed Buddhist practice as constituting a step-by-step ascent toward awakening. Instead, McRae shows that Northern teachers taught something closer to ‘constant practice’ —an approach that anticipates later Sōtō Zen teachings in Japan. For the Northern school, Chan practice was not a means to achieving liberation so much as a moment-to-moment re-cognition and affirmation of what is already the case, that is, of one's abiding *bodhi*.
> 
> – From *Zen Evangelist: Shenhui, Sudden Enlightenment, and the Southern School of Chan Buddhism* by John R. McRae.

This is perhaps pretty good. However, we should note that – notwithstanding whatever shenanigans happened in history – an understanding of the harmony of “sudden” and “gradual” probably goes back at least to the time of Bodhidharma (“Two Entrances”), if not farther, and such an understanding never completely went away.

For example, in *Blue Cliff Record* Case 38: “Feng Hsueh’s Workings of the Iron Ox,” the pointer to the kōan says:

> If we discuss the gradual, it is going against the ordinary to merge with the Way: in the midst of a bustling market place, seven ways up and down and eight ways across.  
> 
> If we discuss the sudden, it doesn’t leave a hint of a trace; a thousand sages cannot find it.  
> 
> If, on the other hand, we do not set up sudden or gradual, then what? To a quick person, one word; to a quick horse, one blow of the whip. At such a time, who is the master? As a test, I cite this to see.
>
> (From *The Blue Cliff Record*, translated by Thomas Cleary & J.C. Cleary.)

Katagiri Roshi discusses this pointer in detail in [“*Blue Cliff Record* Case 38: Feng Hsueh’s Workings of the Iron Ox, Talk 1”](https://katagiritranscripts.net/1982-12-22-Blue-Cliff-Record-Case-38-Talk-1). It is not saying that “sudden” is best or “gradual” is best; once again the point is that we need both, according to Katagiri Roshi. It’s worth noting that the *Blue Cliff Record* originated in the Rinzai school – supposedly identified with “sudden enlightenment.” So the nuanced take on sudden enlightenment here is rather striking, and it is by no means limited to this one case.

Or, for example, in the *Song of the Jewel Mirror Awareness*, we have the lines:

> Now there are sudden and gradual  
> in connection with which are set up basic approaches.  
> Once basic approaches are distinguished,  
> then there are guiding rules.  

Katagiri Roshi comments on this:

> Historically we use the terms Sudden and Gradual to describe the Southern and Northern Schools. The school of Hui-neng is Sudden Zen Buddhism. Sudden means you are already Buddha, so there is a Sudden realization. The school of Shen-hsiu is called Gradual Zen Buddhism. Because you must practice to gradually attain enlightenment, to purify body and mind. So this sutra says there are sudden and gradual, in connection with which are set up basic approaches.
>
> “Basic approaches” means that we should understand the real meaning of the teachings given by Shen-hsiu, founder of the Northern School, and that we should understand through and through the teachings of the Sixth Patriarch, Hui-neng, founder of the Southern School.
>
> – From Katagiri Roshi’s talks on *Song of the Jewel Mirror Awareness* (November 7, 1983 to January 1, 1984), transcribed by Earl Boebert, edited by Jeffrey Broadbent.

Note that again, the “Northern School” and “Southern School” seem to be given equal time. 

So, there is a long history of this view before we arrive at what Dōgen Zenji says in *Bendōwa*:

> Opening the books of scripture is so that, clearly knowing what the Tathagata teaches on the gradual and sudden practices, when we practice in accordance with these teachings, we invariably gain verification of them; it is not so that, wasting our thinking and calculating, we try in vain to assess their merit for attaining bodhi. 
>
> – From *Treasury of the True Dharma Eye: Dōgen’s Shōbōgenzō, Volume I-VII*, by the Sōtō Zen Text Project, p.193.

---

But if we need both approaches, why did Hui Neng become the Sixth Ancestor and not Shen Hsiu? This is a pretty good question, which someone actually asked:

> **Question:** Hojo-san, if in the two poems one isn’t closer to the truth than the other poem, why did the Fifth Patriarch make Hui Neng the Sixth Patriarch, rather than both of them? ... Or neither of them, you know? *[He chuckles.]* 
>
> **Katagiri Roshi:** Because, as Dōgen Zenji mentions, “no buddha-nature” is *pretty close* to pointing out what the truth is. 
> 
> It’s not evaluating both of them, which is right, which is wrong. On the other hand, do you know [the story with] Kassan and Jōzan (Jiashan Shanhui and Dingshan Shenying) in the chapter “Life and Death” (*Shoji* in *Shōbōgenzō*)? Dōgen Zenji quotes two sentences: “If there is a buddha, [there is no life and death]. If there is no buddha, [we are not confused by] life and death.” Something like that; I don’t remember exactly. [...] And then [the two monks] went to see the teacher (Chan Master Fachang of Mount Damei), to evaluate which is right, which is wrong – which is *close* to the truth. Kassan [asks] the teacher, “Which of us is pretty close to the truth?” And [the teacher] says, “Maybe [tomorrow]; please come again.” He didn’t answer. The next day Kassan [comes] again to see the teacher and ask the same question. And then [the teacher] says, “One who doesn’t ask is closer to the truth. One who tries to know which is close is not close.”
> 
> That means “no buddha-nature.” “No buddha-nature” is *pretty* close, pretty close to the buddha-nature. *[He chuckles slightly.]* 
> 
> [This is the same as the story of Hui Neng.] Hui Neng says, “Originally Bodhi has no tree, the bright mirror has no stand.” So it always talks about what the foundation is, and then, “Originally there is not a single thing: where can dust alight?” So constantly his basic foundation is found in *no buddha-nature*, there. 
>
> – From [“*Platform Sutra* – Talk 1” (March 6, 1987) at 1:05:55](https://katagiritranscripts.net/1987-03-06-Platform-Sutra-Talk-1#10555) 

Even so, it’s not one or the other. Returning to the *Song of the Jewel Mirror Awareness*, the next lines say:

> But even though the basis is reached and the approach comprehended,  
> true eternity still flows.  

Katagiri Roshi’s comment:

> This means that if you practice hard, research and study, teach and practice for many years, then you can experience what we call the absolute, or enlightenment. Very slightly you can glance at true eternity, eternal life. You will never be able to explain it, but as a practical matter you will be able to see a little bit of it. That’s pretty good for us.
>
> But if you try to experience this, it will be hard and take a long time, because the eternal life is a really huge mansion. You have to build up that mansion by means of psychology and philosophy and other subjects. And if you start to teach you have to teach this huge mansion, and it really takes time.
> 
> But if you experience it very naturally the eternal life is in your heart. So even if there are some aspects you cannot explain you can still demonstrate the eternal life.
> 
> If people look at someone who has experienced this, for example Shen-hsiu, the founder of the Northern School, they will respect him as a saint. As a pure being. “Even though the basis is reached and the approach comprehended” means that he can walk step by step according to the Buddha’s teaching. True eternity still flows; true eternity is always shown.
>
> – From Katagiri Roshi’s talks on *Song of the Jewel Mirror Awareness* (November 7, 1983 to January 1, 1984), transcribed by Earl Boebert, edited by Jeffrey Broadbent.

--- 

Although it may be helpful to challenge the conventional wisdom on this topic, it’s important to note that the debate over “sudden” and “gradual” is not the primary point in Buddhism, and it could even be seen as a bit of a distraction. In another talk, Katagiri Roshi says:

> Zen history says Sōtō Zen is “gradual enlightenment,” Rinzai Zen is “sudden enlightenment.” It’s ridiculous! *[He laughs.]* If you talk about this, it’s ridiculous. If you’re really crazy about this discussion, you don’t understand Zen Buddhism, you don’t understand Buddha’s teaching, you don’t understand human life. *[He chuckles.]* History is history. Don’t worry about it. If you see someone who is interested in history, let him do that. But don’t be involved in it too much.
>
> – From [“*Blue Cliff Record* Case 45: Chao Chou’s Seven-Pound Cloth Shirt, Talk 1” (May 25, 1983) at 30:00](https://katagiritranscripts.net/1983-05-25-Blue-Cliff-Record-Case-45-Talk-1#3000)

So... heeding that advice, we’ll leave it at that.

```{=typst}
#pagebreak()
```

# Chapter 6: A Hairsbreadth Deviation

## Paragraph 2 Part 1

> 然而毫釐有差天地懸隔、違順纔起紛然失心。  

> And yet, if there is a hairsbreadth deviation, it is like the gap between heaven and earth. If the least like or dislike arises, the mind is lost in confusion. [SZ] 

> And yet, if there is the slightest discrepancy, the Way is as distant as heaven from earth. If the least like or dislike arises, the Mind is lost in confusion. [EB]

## Commentary

The first two characters here (然而) are usually translated as some variation of “and yet,” “however,” “nevertheless,” or “but.” These words are important, as we began to explore in the previous chapter. Here Dōgen presents the other side of the equation: the origin of the way is perfect and all-pervading, *and yet*... Or perhaps we could say, “and also.”

The specific term “a hairsbreadth deviation” appears in the *Song of the Jewel Mirror Awareness*:

> A hairsbreadth deviation  
> will fail to accord with the final attunement.  

Or, put more simply:

> A hairsbreadth deviation, and you are out of tune. 

Katagiri Roshi comments on this: 

> If you miss the beat even slightly you cannot fit into the rhythm of music. You slip off. So regardless of whether we understand or not, our practice is to try to tune into the rhythm of music.
> 
> Regardless of whether you understand or not, you should keep your eyes open to how to tune in, because you are Buddha. Because you have to grow that seed of buddha nature. So you have already a great rhythm of music in your heart. Trying to tune into it is our practice. If you don’t, immediately there is a gap. That slight gap is huge, like the gap between heaven and earth. So it is pretty hard to live in peace and harmony.
> 
> In the *Shōbōgenzō* Dogen Zenji says that if you wish to understand the seed of buddha nature you should know that it is precisely the causal conditions of time and season. That is a big term; practically speaking it means time and space becomes fresh from moment to moment. It means there is no constant name that can apply to you. Good, bad, whatever. Nothing. Always you are fresh. So you have to live in this state of freshness. That is Buddhist logic.
>
> – From Katagiri Roshi’s talks on *Song of the Jewel Mirror Awareness* (November 7, 1983 to January 1, 1984), transcribed by Earl Boebert, edited by Jeffrey Broadbent.

--- 

Discussions of *a gap* or *separation* are fundamental in Katagiri Roshi’s teaching – so much so that those terms appear in well over half of his talks. Equally numerous are discussions of the opposite, which would be *samadhi*, “one-pointedness,” or “total acceptance,” et cetera, which are how we live in the state where “time and space becomes fresh from moment to moment,” as he says above. Or as he says in [“Fukanzazengi – Talk 1” (June 9, 1979),](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1) “You must accept zazen as total activity which is vividly alive from moment to moment.” We also call this *freedom*, or *liberation*.

The gap is the discrimination of consciousness, the mind. It seems to come down to, this is how consciousness works. This is what Katagiri Roshi calls *the dualistic world*. 

One good discussion of this is in a talk on *Blue Cliff Record* Case 51 – where, one might observe, someone raises almost the same question as Dōgen:

> **Question:** Um, I have a question about... A lot of times I wonder why I’m on this path, and why humans constantly are looking for enlightenment, or going back to the true life. How did we ever get off the road? Why? Is it just solely to learn? Or... why? Why did we ever come out, why did we ever try to separate ourselves? 
> 
> **Katagiri Roshi:** Separate from ... ?
> 
> **Questioner:** From the life force. Why [do] we choose to pretend like we’re separate from the oneness? 
> 
> **Katagiri Roshi:** Uh-huh. Because we have a mind. We have consciousness. 
> 
> The energy of the consciousness is to separate, analyze, you and object and everything. This is the energy of consciousness and your mind.
> 
> So very naturally, you can slip off from the life force itself. On the other hand, by analyzing, synthesizing, and trying to understand your object and yourself, then that is called *the self*. 
> 
> You know that Descartes says, “I think, therefore I exist.” Okay? *[He chuckles.]* So, you cannot ignore that energy of mind. Thanks to the energy of your mind, you can appreciate the presence of the self. 
> 
> That is called *self*. But the energy of the self means the quality of the self has the great power to bring the harmony to your life – looking at this life, so-called present, and past, and future, including life and death. This is the energy of the self. 
> 
> Energy of the self is very powerful because [we are not only] looking at *this* life, in terms of making [a] better living, conflicting with or fighting each other – not like this. Like birds, and insects, and woodchucks. 
> 
> I always say, “woodchuck.” *[He laughs.]* (*Transcriber’s Note:* It seems possible he means “squirrel” here.) Woodchuck is always living in the trees, and dogs walk under the tree – immediately, *[whoosh]*, you know? But this action is to see his life in terms of instinct. He is always looking at his life [as] just a small world, in terms of instinct. 
> 
> But the energy of the self is very powerful to look at this life and [other lives], all the world – understanding as a whole, as a one. That is a quality of the self. That quality of the self is very vital. So that is called *energy*, *life force*. 
> 
> Life force itself is simultaneously birth, your life. Life force is something coming up [...]. That is just like spring water gushing out from the ground. 
> 
> So “let’s return to the source” means life force [is] constantly gushing out. That is, when [...] life force comes up, it is called *birth*. And when you are born in this world, simultaneously you have a mind and consciousness. So [you] analyze, synthesize. [...] In other words, the energy of the consciousness and mind comes from life force itself. You cannot ignore it. 
> 
> So thanks to the life energy of the consciousness [...] you can see, you can justify, you can confirm *you*, so-called *the self*. That energy of the self is not looking at only this life, but a big world: past, present, future, *as a whole*, as a one. This is the energy of the self. 
> 
> And then if you understand like this, then we can return to this energy again. That is called *spiritual teaching*. 
> 
> So...
> 
> So. 
> 
> *[Laughter.]*
> 
> No particular reason why we have to do it, because we already are there. So all we have to do is just to learn where we are: what is the self, what is the consciousness. Not analyzing [and] synthesizing the consciousness, but by the consciousness we should know the limitation of the consciousness. *[He chuckles.]* In other words, through the consciousness we should learn what the consciousness is. Because consciousness is nothing but the energy of life force. 
> 
> So we should learn through the consciousness. Very naturally you can know limitation of consciousness *by* the consciousness. *[He chuckles.]* Alright? 
>
> – From [“*Blue Cliff Record* Case 51: Hsueh Feng’s What Is It? – Talk 2” (January 18, 1984) at 1:06:30](https://katagiritranscripts.net/1984-01-18-Blue-Cliff-Record-Case-51-Talk-2#10630)

This matter of the energy of life coming from the “self” – and here we are not entirely talking about “Big Self” with a capital S – is deep. This is Buddhist psychology, and it is pervasive in Katagiri Roshi’s talks. In particular, in the Yogachara school of Mahayana Buddhism, this relates to the seventh of eight consciousnesses: *manas*, which Katagiri Roshi translates as “ego consciousness.” It’s outside the scope of this presentation, but among the best places to start studying this is in Katagiri Roshi’s series of talks on Dōgen Zenji’s [*Genjōkōan*](https://katagiritranscripts.net/genjokoan), which includes an entire talk on *manas*.

“Like” and “dislike” are also part of consciousness, cognition. The specific phrase “like or dislike” appears in perhaps over a hundred of Katagiri Roshi’s talks. We’ll return to how to work with like and dislike, good or bad, et cetera, in Chapter 9: “Take the Backward Step,” Chapter 15: “Have No Design on Becoming a Buddha,” and probably in many other places.

--- 

Katagiri Roshi also mentions mentions “the gap between heaven and earth” in the same talk on *Blue Cliff Record* Case 51. The pointer to the case says: 

> Even if you arrive immediately at the point of solitary liberation, you haven’t avoided looking back to the village gate from ten thousand miles away.

Katagiri Roshi comments:

> “Even if you arrive immediately at the point of solitary liberation” means [even if you have] oneness of the mountain and you who are climbing the mountain – you say, “I get it!” You get exactly a feeling of oneness, but at that time it is already something you can see objectively, so that oneness is not *real* oneness. That oneness is *perception* of the oneness, not *the last word* of the oneness. The last word of the oneness is constantly you must be alive right in the middle of oneness. *Constantly*. 
>
> If you *think* it, that is you immediately create a huge gap, just like between heaven and earth. That’s why here it says, “Even if you arrive immediately at the point of solitary liberation, you haven’t avoided looking back to the village gate from ten thousand miles away.” Anyway, you are just haunting the [fields and forests]. It’s a [ghost story]. 
> 
> The other day I went to Milwaukee, and one of the Tibetan Buddhist groups taught me a very interesting... I don’t want to tell this story because it’s a little bit... I’m hesitating. *[He laughs a little.]* But anyway, whatever [this person] does, he is always very strongly imaginative about Avalokiteshvara, [the bodhisattva of] compassion. He tries to create the energy of Avalokiteshvara, so-called compassion, whatever he does. Particularly when he has excitement, right in the middle of excitement, he tries to create energy of Avalokiteshvara’s compassion. And then he feels pretty good! So he asked, “Is that right?” I said, “Yes, or no.” 
> 
> Well, in a sense it’s pretty good, but in a sense it’s nothing but a ghost depending on the trees and grasses: depending on the imagination of Avalokiteshvara, and “haunting” the excitement, spiritual fascination. If you are really stuck there even a moment, you just look at that experience; it’s not the last word of peace. Peace and harmony is not something coming from outside, but from you. Not *from* you... *in* you. *You* are peace. You must be peace itself. 
> 
> So even if you constantly practice like this, and even if you feel good because you can get the energy of compassion or you can get the energy of your life, it is still [an imaginary] world. Because it is nothing to do with real peace of you. Because you are still swayed away by imagination of energy, or spiritual fascination, or excitement... many things. Feeling good or not feeling bad, always. But real peace is you must be the last word of your being, *exactly*. 
> 
> – From [“*Blue Cliff Record* Case 51: Hsueh Feng’s What Is It? – Talk 1” (January 11, 1984) at 51:32](https://katagiritranscripts.net/1984-01-11-Blue-Cliff-Record-Case-51-Talk-1#5132)

The mind is sneaky: we can attach even to the concept of liberation and compassion. That makes Buddhism kind of hard. But it’s also simple: just be right there.

This topic comes up a lot. In fact, it will come up again in the very next chapter.

```{=typst}
#pagebreak()
```

# Chapter 7: Playing in the Entranceway

## Paragraph 2 Part 2

> 直饒誇會豐悟兮、獲瞥地之智通、得道明心兮、擧衝天之志氣、雖逍遙於入頭之邊量、幾虧闕於出身之活路。  

> Suppose you are confident in your understanding and rich in enlightenment, gaining the wisdom that knows at a glance, attaining the Way and clarifying the mind, arousing an aspiration to reach for the heavens. You are playing in the entranceway, but you are still short of the vital path of emancipation. [SZ] 

> Suppose one gains pride of understanding and inflates one’s own enlightenment, glimpsing the wisdom that runs through all things, attaining the Way and clarifying the mind, raising an aspiration to escalade the very sky. One is making the initial, partial excursions about the frontiers but is still somewhat deficient in the vital Way of total emancipation. [EB] 

## Commentary

Mahayana Buddhist teaching talks about the “vibration of the mind,” including the very subtlest vibrations. The basic issue is, this finest vibration never goes away. Katagiri Roshi says: 

> For instance, according to *The Awakening of Faith*: at the *tathāgata* stage, Buddha knows the finer of the fine vibration of the mind. Among the fine vibration of the mind, there is the *finest* vibration there; very minute vibration of the mind. Because mind is constantly moving. Even though you say *moment* – the *Abhidharmakosha* says the moment consists of 65 instances. If so, what is a moment, you know? So the moment is a very fine vibration of the mind, but still there is the finest vibration of the mind within the moment – that is at the 65th vibration of the mind. How can you touch it? You don’t know what it is. But it’s there. Through zazen you can notice this.
> 
> So, if you are engaged in a perfect state of concentration, let’s [look at] your mind in zazen. Then you really feel exactly the planting into *samadhi*. But still you can see the very minute vibration of the mind, so-called “perfect concentration,” “perfect state of planting into *samadhi*.” You can see: “Oh, I am planting into the perfect *samadhi* now.” Something like this is the very minute vibration of the mind by which you can realize what you are doing, what is mind. 
> 
> But no matter how long you recognize this minute movement, vibration of the mind, you never be free from vibration. No; because even though you say, “I am perfectly calm now” – that is already vibration. *[He laughs.]* So “thinking not thinking” begets thinking. Realization of the perfect *samadhi* begets vibration of the mind. So you are never free from vibrations. 

That’s the issue. But if we stopped there, it might be a bit of a downer. Katagiri Roshi continues:

> So how do you be free from this very minute vibration of the mind, from moment to moment? It’s very difficult to say *how* you do it. No, we don’t know. But this is the *tathāgata* stage, according to *The Awakening of Faith*. It is true! So finally, that is the place [where] the one world, where the very minute vibration of the mind can be realized: by buddha-*tathāgata*. At that time, buddha-*tathāgata* knows how to live there. 
> 
> Because whatever you think, no matter how long you cognize or you realize that very minute vibration of the mind, you never stop vibrating your mind. So how do you stop vibrating your mind? This is, it’s very simple, *very* simple. It’s very simple, but it’s too simple to know. *[He laughs.]* So all you have to do is just *be there*. 
> 
> Just be. *Tathāgata* stops vibrating. “*Tathāgata* knows how to stop vibrating” means just *be* exactly – with no second person, no second thought. This is total dynamic working. You become exactly one.
>
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986)](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4)

So, you can do it – or *tathāgata* can do it. What you can’t do is attach to it. It’s not something that “you” get to “have.”

---

Katagiri Roshi discusses “raising an aspiration to escalade the very skies” when he gives the talk on *shō*, “realization,” which we referred to in Chapter 3:

> So that is the place where all living beings coexist in peace, and ... synchronize with each other in peace and harmony. That is *shō*, “realization.” 
> 
> So that *shō*, the consummation of being, is not [something] you try to manifest. No, you cannot do it, because this is exactly the *ultimate* state of existence. You don't know [it]. But the unique way is to let it manifest by virtue of making your water clear or calm. Or, practically speaking, you really devote yourself to do something thoroughly, with sincere heart, *exactly* do it: then, the consummation of being comes out, emerges from [that] naturally. That is our practice. 
> 
> But we always try to get that truth or consummation of being. We try to get it. That's why we say, “By practice, let's attain enlightenment.” That makes you *more* confused. It's pretty hard to get such enlightenment. Of course you can attain enlightenment, but that enlightenment is the first or second enlightenment I mentioned: *kaku* or *satori*. Still *kaku* and *satori* are nothing but a human experience, limited by individualities. So it's not universal. Universal enlightenment is the state of being free from individual experience called *kaku*, awakening, or *satori*. According to Buddha's term, it is called *nirvana*. Nirvana. So *nirvana* corresponds to *shō*: proof, or verification. 
> 
> So *nirvana* is a place where all kinds of experience of highest spiritual life are melted into. That is called nirvana. In other words, all kinds of the highest level of spiritual life is liberated. And then it is called *nirvana*. That is called *total liberation*. 
> 
> So that's why ... even though you don't experience this *shō*, the actualizing the consummation of being, even though you don't experience the ultimate nature of existence... as best as we can, we try to approach it, we try to come near to it. In many ways – psychologically, intellectually – in many ways we try [to] see even a dim image. As close as you can, you try to approach. That is our study.
> 
> And then, [...] to touch directly the ultimate nature of [your self] is your responsibility, your business. Your responsibility, so-called ... flow of activities – when you are exactly in the continuous flow of activities, and then you are there, exactly. [But] consciousness always slips off this flow of activities, and analyzes, synthesizes, so that's why it's pretty hard to touch directly. 
>
> So that's [where] in *Fukanzazengi*, [...] Dōgen Zenji [says], 
>
>> Suppose one gains pride of understanding and influences one’s own enlightenment...
>
>So, by zazen, you can attain awakening and enlightenment, *satori*, and then you are proud of yourself. Then he says, that’s fine, but:
>
>> Suppose you gain pride of understanding and influence your own enlightenment, glimpsing the wisdom that runs through all things, attaining the way and clarifying the mind, raising an aspiration to escalade the very sky.
> 
> *[He laughs.]* Do you understand? That always happens in the religious world. Always you really go up to the sky, pretty high. And then you completely forget to come down to earth. *[Laughter.]* But the more you try to stay high in the sky, impermanence ... lets you fall down to the earth, and then at that time you hurt so much. *[He laughs.]* Because you are too high to come down, so you hurt so much. 
> 
> Just like a helicopter, you know? *[Laughter.]* Each person is flying a helicopter, with three propellers: [...] *suffering* and *karma* and also *self-centeredness*. The three propellers run pretty fast, and then finally, everyone can fly in the sky. Each person can fly, and then he likes it, you know? Because he [doesn’t bother himself], he always keeps himself in peace and harmony, keeping away from the people. So he tries to do many things as he likes; that’s [what] everyone does in the sky, in the world. And then – they bump into each other, by chance. And then it hurts very much, you know? Sometimes one propeller is broken and then, boom, they fall to earth, and then it hurts so much. This is suffering; always we do [this]. 
>
> That’s why Dōgen Zenji says here, 
>
>> ... raising an aspiration to escalade the very skies. One is making the initial partial excursions about the frontiers, but is still somewhat deficient in the vital way of total emancipation.
>
> So still a little far, a little far. 
>
> So, very naturally, the important point is [that] practice must be total manifestation of ultimate nature of existence, and ultimate nature of existence is simultaneously present with your practice. Because ultimate nature of existence is not your business. It is not something *you* try to manifest. No. You have to arrange circumstances, [arrange] your body and mind to be in peace and harmony, and then, ultimate nature of existence comes out naturally. Like the moon comes out from the clouds. Like this. 
>
> – From [“*Bendōwa*: Dōgen's Questions & Answers – Talk 5” (March 15, 1987)](https://katagiritranscripts.net/1987-03-15-Bendowa-Talk-5)

So by zazen you can attain awakening (*kaku*) or enlightenment (*satori*), but these are still temporary, limited experiences – and coming down from them can be a bumpy ride.

--- 

Later in the same talk Katagiri Roshi is asked whether *kaku* “awakening” and *satori* “enlightenment” are important.

> **Someone:** Is there a progression between these stages? Awareness, enlightenment, verification: is there a progression, and are those stages of growth? 
> 
> **Someone:** So you go through one first, *kaku* first, then *satori*, [...]
> 
> **Katagiri Roshi:** I think so. Uh-huh.
> 
> I think *awakening* is used in English textbooks in many ways. But generally speaking, *awakening* is the first experience of spiritual life through the six senses. Okay? And then enlightenment, *satori*, is a little deeper than awakening, penetrating. You have to experience *satori* [...] through the body and mind. But awakening kind of comes through the consciousness; then you can awake. So *awakening* occurs in the conscious level, but *satori* occurs in the conscious and also physical levels, both. So a little deeper. 
> 
> **Question:** But... there’s *shō*, even if you don’t experience *kaku* or *satori*, isn’t there?
> 
> **Katagiri Roshi:** Yeah, *kaku* and *satori*...
> 
> **Question:** How important are they? 
> 
> **Katagiri Roshi:** *Kaku* and *satori*? 
> 
> **Question:** Yeah.
> 
> **Katagiri Roshi:** Well, important. But people really try to hold on [to] *kaku* and *satori*, which seem to be a best experience. That’s why Dōgen Zenji [says] that’s why people are proud of themselves very much. They are proud of their understanding, their own experience, but this is nothing but escalading for the sky. *[He laughs.]* Going up to the sky, that’s it. That’s why under the beautiful flag of religions, we are always fighting. If you experience God, then you are proud of your experience and understanding of God, and then we become really high. That is really a problem for us. Finally, fighting. 
> 
> So [the] most important point is, you must be liberated from that pride of your understanding of God, and Buddha, or enlightenment, or whatever. And then, you really become humble. You know? And also majestic. Very majestic and humble. And then you can help people. Otherwise, you create problems. That’s what Dōgen Zenji says here.
> 
> So I don’t mean *satori* and awakening are not important. They are very important for us. 
> 
> **Questioner:** So, [...] *shō* was somehow always there. 
> 
> **Katagiri Roshi:** Always there!
> 
> **Questioner:** It’s always present, while *satori* or awakening are not necessarily always there. 
> 
> **Katagiri Roshi:** *Satori* and awakening are kind of bubbles coming up, you know?
> 
> **Questioner:** Yes, [...] to experience it is important. But is it possible to realize [or] experience *shō* fully if you haven’t experienced *satori* first? 
> 
> **Katagiri Roshi:** I don’t know which comes first. I think first, basically, *shō* is there, from the beginning to end, always. And then, under the certain circumstances, you can call it *awakening* sometimes, you can call it *satori* sometimes. Sometimes you cannot call it at all. That is *shō*. No name there, but you feel strong, on the basis of your life. You don’t know what it is, but you feel strength. 
> 
> **Questioner:** So are you saying that *satori* or awakening is not really necessary if you... ? 
> 
> **Katagiri Roshi:** Well, it’s necessary, but I don’t think you should try to hold [them] always, try to get a hold. No. But you shouldn’t ignore the *satori* and awakening. The point is you have to focus on that point, *shō*, where we are. Because we live there. So [focus on] where we are, and then we should take care of our life. 
> 
> But usually, we always try to live in the realm of awakening or *satori*, and *then* we try to take care of human life. That’s why [we are] more confused there. But we should focus on the very basic foundation, there, and then you can deal with *satori*, awakening, and many things. That’s [what] Dōgen Zenji tries to present always. But this is not Dōgen’s teaching, this is a general Buddhist teaching. [It’s] why Nāgārjuna mentions 18 emptinesses, you know? *[He laughs.]* Why he has to say 18 emptinesses, 25 emptinesses, constantly. It’s ridiculous! *[He laughs.]* But he has to say [it]. 
>
> **Someone:** Excuse me, Roshi. Could you clarify what the difference is when you say this is a Buddhist view versus this is Dōgen’s view? 
> 
> **Katagiri Roshi:** Well, Dōgen’s view is a more practical point. He gives suggestions how to practice it, how to [make] Buddha’s teaching alive in human life, practically. That’s always what Dōgen Zenji [talks about]. So he has very deep thought, [...] and his practice is backed by this deep thought – that’s why people say Sōtō Zen’s [or] Dōgen’s philosophy [is] “scholastic.” I don’t think he is “scholastic.” *[He laughs.]* He is a pretty religious, genuine person. 
> 
> So he always puts it into practice, and then be free from thought, because deep thought is always working in his life as a religious life. So that’s why his practice is very deep. But on the other hand, it’s really manifested, so it’s just like everyday practice. 
>
> – From [“*Bendōwa*: Dōgen's Questions & Answers – Talk 5” (March 15, 1987) at 33:02](https://katagiritranscripts.net/1987-03-15-Bendowa-Talk-5#3302)

---

A danger here is that even when we realize that awakening and enlightenment are temporary, we can still attach to realization or *shō* as just another concept, and we can use it to criticize ourselves or others. Katagiri Roshi talks about this in one of his talks on *Genjōkōan*, with a special caution for priests:

> **Question:** Hojo-san, when you’re mentioning that when you’re behaving morally and ethically you say “I’m a very good boy,” “good saint” and so forth, and then that’s ego – at the moment that you realize that that’s ego coming in, is that *manas*?
> 
> **Katagiri Roshi:** Yes, ego.
> 
> **Questioner:** Realizing that it’s ego (is ego)?
> 
> **Katagiri Roshi:** Yes; ego is *still* working there! Even though you do zazen and are constantly seeing and feeling who you are, how ego is working very deeply, still ego is working. So that’s why very naturally pride is coming up; it’s very difficult to be patient, or it’s very difficult to be humble. Always there is ego. Even if you see the truth, [...] you attach to it even more, because it’s very beneficial to you. Ego consciousness realizes how beneficial realization of *alayavijñāna* is, and then *attaches* to it. *[He laughs.]* And then *manas* brings that attachment into the six consciousness world. 
>
> And then, at that time, manas really forces you to get everyone to believe something you have. That’s why, if you believe something religiously, you’re always forcing people, in many ways: “You should believe *this*; if you don’t, you are stupid.” *[He laughs.]* 
>
> Always [this is going on]; not only the religious world. [But] if you deal with religion, it’s very dangerous, because you don’t realize how hurt people [can be] through this ego. In the usual [world], it’s very quick, and everyone expresses ego – that’s why you don’t feel how much you hurt people, because *everyone* does it, you know? [We say,] “You should express your ego; if you have a capability, you should express it.” If you don’t feel good: scream, scream. Everyone screams, so the whole room is screaming. Even if only one person screams, everyone says, “Oh, you’re screaming.” So your screaming doesn’t hurt so much, because everyone does it. *[He laughs.]* 
>
> The religious world is more complicated. *[He laughs.]* If you see the religious world, so-called peace and harmony, through *belief*, then you attach strongly. And also the problem is that no one [else] experiences it; everyone behaves in a different way from you. That’s why you strongly believe the truth after practicing hard for many, many years, and then you really attach to your experience, or career, and belief; then finally you put everyone down, because everyone is doing it in a completely different way. So very naturally, if you want to save people, help people, you *force* them. If people don’t follow it, you fight. That always happens. It’s very dangerous. Spiritual fighting is really *miserable*. 
> 
> So that’s why we have to realize ego consciousness through meditation, and then you can feel directly who you are. And then, *manas*, ego consciousness, has *alayavijñāna* as [its] object, which means you feel karmic life through realization of manas. You can see.
> 
> How can you take care of your life? Sometimes, there is no way. Katagiri is Katagiri; no matter how long I study Buddhism, still [there is some] smell; I can’t escape it. But, this is Katagiri’s; this is a [way] for Katagiri. *[He laughs.]* But I don’t [mean] it is a goal, what I have to do. Next, I have to go farther, deeper, until realizing *alayavijñāna* as *tathāgatagarbha*. That means completely you have to touch the base of *manas*. You should directly experience stream energy. Directly, okay? In other words, you must be *on there*; you must be right there. Instead of understanding through conceptualization – no. Consciously or unconsciously you always understand in a conceptualized [way], but it is not the experience of alayavijñāna. You have to directly be right there, beyond the world of conceptualization. 
> 
> Where you should be present is right there. That is the stream of energy, the flow of energy. And then, at that time, this is really *cosmic*. So wherever you may be, all you have to do is just be there, and go. But that is nothing to hurt anything, because in that realm of the world, all sentient beings are included. So [there is] nothing to hurt; if you hurt something, you fall away from it. 
> 
> So that is the bodhisattva category and buddhas category [that] you should learn. This is the advantage of practice for human beings. 
>
> [...] If you are a priest, you should taste and chew and digest what I told you today again and again. And then read this *Genjōkōan*; then you can really feel the spirit. 
> 
> One more thing. Usually people say, “You should attain enlightenment. You should be aware. If you’re not aware, if you don’t realize, if you don’t attain enlightenment, you are not Buddhist; you are a stupid guy.” *[Laughter]* That is not the Buddhistic way; no. It’s a complete misunderstanding. Alright?
> 
> So, please [try to] understand what I have said today again and again. And then, if you understand what I said: [...] even if you attain enlightenment, originally where [are you]? “Originally” means very basically, profoundly, where [are you] standing? Are you standing in the realm of six consciousnesses, or seventh consciousness? Yes, you are... but simultaneously, the very source of your presence is *alayavijñāna*, *tathāgatagarbha*. What is that? That is just the flow of energies, which is very pure and clear. So that is called *you are Buddha*, where all sentient beings exist just like that. 
>
> We should learn that, okay? Basically, profoundly, you are already present there; that’s why even if you attain enlightenment, still there is opportunity or possibility to manifest this. So *how*? That’s why I say, finally, when you do gassho, please do gassho. That’s it!
> 
> Dōgen Zenji says from the beginning [it is] just like this. It’s a little bit difficult to understand; that’s why you should digest what I said again and again. Then, if you get into this *Genjōkōan*, it’s a little bit easier to understand. 
>
> – From [“*Genjōkōan*: Talk 2” (June 6, 1987) at 47:12](https://katagiritranscripts.net/1987-06-06-Genjokoan-Talk-2#47:12)

```{=typst}
#pagebreak()
```

# Chapter 8: Buddha and Bodhidharma

## Paragraph 3

> 矧彼祇園之爲生知兮、端坐六年之蹤跡可見。少林之傳心印兮、面壁九歳之聲名尚聞。古聖既然、今人盍辦。  

> Consider the Buddha: although he was wise at birth, the traces of his six years of upright sitting can yet be seen. As for Bodhidharma, although he had received the mind-seal, his nine years of facing a wall is celebrated still. If even the ancient sages were like this, how can we today dispense with wholehearted practice? [SZ] 

> Need I mention the Buddha, who was possessed of inborn knowledge?
the influence of his six years of upright sitting is noticeable still. Or Bodhi-
dharma's transmission of the mind-seal?—the fame of his nine years of wall-
sitting is celebrated to this day. Since this was the case with the saints of old,
how can men of today dispense with negotiation of the Way? [EB]

## Commentary

Why was the Buddha “wise at birth,” having “inborn knowledge”? Perhaps it’s something like what Katagiri Roshi spoke about on Buddha’s Birthday:

> ... you know in the [story], when the Buddha was born – do you remember? The Buddha walks seven steps, saying, “I alone am the [...] honored one in heaven and on earth.” 
> 
> He walks seven steps. Why does he walk seven steps? This is also a legend. 
> 
> The number seven is a holy number, according to *Rigveda*. In India, *Rigveda* is a very old Indian philosophy. If you study Indian philosophy, you have to read the *Rigveda*. It’s very wonderful... I forget the name, but it’s very nice in Indian philosophy. In the *Rigveda*, I think the seven holy men command great respect from the people in the scripture, and then from that point the number seven becomes a holy number. So that comes into the Buddhist tradition: so-called the seven past buddhas, before the Buddha was born, who were the Buddha’s teachers. 
> 
> So we say [there were] seven buddhas in the past, before Buddha was born, because even though we don’t have any historical proof [or] historical references, as long as Buddha was born here in this world, I think there had to be the past. In other words, as long as you exist today in the present, I think you should have a past. If you see the present, the present brings on the past and also the future, and *then* you can see the present. Through the present you can see the past, you can see the future; in other words, we may reverse the order and say the present is supported by the past and future. So if you accept Buddha’s existence, very naturally he has a past. That is the seven buddhas before Buddha was born.
> 
> So that’s why seven is a holy number, [and] that’s why we say in the legend the Buddha walks seven steps. Why does he walk seven steps? Because people believe that he is a human but he is not human, [he is] something more than human, who is great, beyond human speculation. That’s probably why he walked the seven steps the moment when he was born. It’s impossible for us as humans, but he is [both] a human but he’s not human, because he is *great*. Can you see [this]?
> 
> Well, this is natural, from human feeling. For instance, if you become *great*, more than usual people, people really believe [in] you. Even though you move your hand in the same way as people do, your moving is special. Do you understand? *[He laughs.]* Katagiri smiles, and Katagiri smiles in the same way as you smile, but if you really believe him, trust him, and pay homage to him, exactly his smile is completely special. And from that smile, you know, the light [comes] forth. *[He laughs.]* Do you understand that human feeling? Yes, it is natural! But if you don’t [exactly] trust some person, even though he smiles in the same way as people do, you hate it, you hate his smile. But his smile is the same thing! *[He laughs.]* 
> 
> So, that’s why he walks seven steps. Seven is a holy number. Anyway, he walks from the [mother’s] belly. [That] means he is something special: walking in the human world, walking hand in hand with all sentient beings, [even as a] baby. 
>
> And also he says, “I alone am [the] honored one [in heaven and on earth].” This is not individualism, okay? This is not egoism. It [does not mean] egoism; it is the implication of thoughtfulness, kindness, or compassion to *all*, because *all* are great, completely great. No one hurts or destroys that greatness [inherent] in everyone and all things – trees, birds, nature, pebbles, waters, et cetera. Everything has greatness, [the] so-called *lifeline of buddha*. Exactly the same lifeline [that] Buddha Shakyamuni has. 
> 
> That’s why this is called – maybe in the usual terms we say [a] *human right*. [If we] say [a] *human right*, it is a very usual word, but religiously we are *great*, beyond human speculation, human judgement. That’s why we have to respect [others], or we have to put ourselves in others’ place, and be thoughtful, be kind, be compassionate to human beings, and also to everything. 
> 
> – From [“Buddha’s Birthday” (April 13, 1986) at 10:16](https://katagiritranscripts.net/1986-04-13-Buddhas-Birthday#1016).

---

But even with that inherent greatness (which everyone has), “the traces of his six years of upright sitting can yet be seen.” Even though we can’t attach to any result from practice-realization, those results do appear. There is a kind of maturation that happens naturally in practice.

Katagiri Roshi talks about maturing or deepening our life in most of his talks. Here is one example:

> The other day I told you, when you want to be great mountaineer, you have to be one with the mountains. How can you do it? Just climb; climb the mountain. Every day; even in the snow. In winter and summer, we have to be one with, be present with the mountains. 
> 
> To be present, be one with the mountain is to make your life deepen and mature. If your life is mature, very naturally you can live with the mountain exactly in the same way as the mountain’s life. So, mountains give your maturity to you. 
> 
> How can you know? You try to climb the mountain constantly. 
> 
> Well, whatever you do, this is a very basic practice for us. 
> 
> – From [“Blue Cliff Record Case 51: Hsueh Feng’s What Is It? – Talk 2” (January 18, 1984) at 33:16](https://katagiritranscripts.net/1984-01-18-Blue-Cliff-Record-Case-51-Talk-2#3316).

---

Katagiri Roshi often talks about the ripening of the persimmon. Here he is talking about Chao Chou (Jōshū), who was himself a semi-legendary figure in Zen:

> Maybe you can understand the progress of human life in terms of three points. One point, the first stage, is fruit. Second, the ripeness of fruit. [Third], the perfect ripeness of fruit.
> 
> For instance, a beautiful persimmon on a tree – that is a fruit. That is awareness of buddha-nature, or awareness of how important human life is, how sublime human life is. So you respect yourself, you respect others. That is the first stage. That is a fruit.
> 
> And then, gradually this persimmon is getting ripe. So, pretty sweet. Not *exactly* sweet, not *exactly* ripe, but it’s ripe. That is the second stage. When you study hard and practice hard, then your personality, your human life is getting ripe. And then [you are] understanding people pretty well, and also yourself.
> 
> And the third stage: when the persimmon is completely ripe on the branch, very naturally that persimmon falls down to the ground, and the guts of the persimmon come out. Do you understand that one? *[He chuckles.]*
> 
> That’s pretty nice. “Guts come out” means whatever it is, whatever you want, everything comes out, but it [isn’t] against any rule and the reason of nature, and [it is] exactly going smoothly. That means *egolessness*. According to egolessness everything comes out. So, perfect maturity of human personality.
> 
> That is the three stages.
> 
> So, the ripeness of the fruit is not good enough. Because, for instance, finishing high school or university, and getting the degrees, [like] doctorate degrees – it’s *ripe*, but it’s not ripe *exactly*. After that you have to polish yourself again and again. And then, maybe [...] you can let your life mature and ripen, so then you become a great medical doctor et cetera as a human being, because you can help. 
> 
> But it’s not good enough. So, you have to make your life *more* mature – until the mature fruit falls down to the ground and all the guts come out. That means your personality is not only working in your territory, so-called [field of] medicine, or psychology, or music – but also, when your maturity is perfected, completed, at that time your mature personality is working everywhere, even in daily routine, even out of your music area or psychological area as a professional. Wherever you may go, your life is really working smoothly.
> 
> That is called *freedom*, *emancipation*. Or *maturity*. Or *adept*.
> 
> I think Chao Chou in this koan is really mature and perfect ripeness of fruit. Everything is going pretty smoothly, naturally. So nothing sharp in the words. He uses words, but those words are not very sharp. Priests’ words come up very naturally, smoothly. But lots of information is there, instruction is there.
>
> – From [“*Blue Cliff Record* Case 52: Chao Chou Lets Asses Cross, Lets Horses Cross – Talk 1” (January 21, 1984)](https://katagiritranscripts.net/1984-01-21-Blue-Cliff-Record-Case-52-Talk-1).

---

So when we reach a certain stage of maturity – perfect ripeness of the persimmon – we can stop, right? 

No. 

Katagiri Roshi says:

> So we have a karmic life. Everyone is different; everyone is characterized by karmic life of their own. But it is not *wrong*, it is not *right*. Sometimes we really respect a person who [renounces] his or her own karmic life; then we really respect them as a “saint.” I don’t think it is right. I don’t think it is wrong; it’s fine. But Buddhism doesn’t say karmic life is wrong, karmic life is right; no. The point is we should constantly *deepen* karmic life, because karmic life is Buddha. 
> 
> And then we say, “Karmic life [is] Buddha, so why don’t you accept karmic life?” No. If you say so, you stay on the chair of buddha. So you never have a chance to deepen the stage of the buddha. Buddha is not a *stage*, buddha is constantly great energies to encourage you to deepen, to taste your life. And then, you can create *total, whole personality*, from which you can really educate, nurture you and everyone. 
>
> [...] So we should respect [great capacity], but I don’t think we should be proud of ourselves, “I am great.” At that time, you know, the deepening of your life *stops*. You stop deepening your life, deepening the experience. 
> 
> That’s why the more you become a master of something, the more you continue practicing. You can see people like this: the more they become a famous pianist or dancer, the more they’re always practicing, because there is no reason why they have to stay at a certain stage, and showing [that they are] proud of their life. No way; constantly deepening his or her experience of dancer, music, et cetera. 
>
> – From [“*Platform Sutra* – Talk 7” (April 24, 1987) at 33:00](https://katagiritranscripts.net/1987-04-24-Platform-Sutra-Talk-7#3300)

---

And also, this kind of maturation does not happen alone. Here we again see the connection between zazen and the Precepts:

> [Kyōgō Zen master says,] “In attaining enlightenment under Bodhi tree Shakyamuni Buddha fruited the precepts.” Shakyamuni Buddha did not try to fruit the precepts; *fruit* is [that] naturally something is matured, nurtured. Not only by one person; no, you cannot mature anything [that way], you cannot ripen anything by yourself. You need lots of help. You know, others: trees, birds, all sentient beings, past, present, future. All sentient beings [are there], *then* something is ripened. 
> 
> You can see the fruit on the tree. You say, “Oh, fruit!” No one pays attention to the depth of the fruit’s life, how fruit becomes fruit; we don’t pay attention to it. And then immediately we pick it up and eat it. That is really a hungry ghost attitude, you know? *[There are some chuckles.]* 
> 
> That is important: A precept is not something produced or created by somebody or something. Realization of the whole universe, how it is going: fruit ripens. The person’s life, tree’s life, and all sentient beings, that is called *precept*, we say. First, you should remember this [point].
>
> – From [“The Way of Precept Practice: Restraint and Extermination” (August 13, 1988)](https://katagiritranscripts.net/1988-08-13-The-Way-of-Precept-Practice-Restraint-and-Extermination)

---

Bodhidharma was the First Ancestor in China, the prototypical Zen Master. This is how Katagiri Roshi tells the story on one of many occasions: 
 
> When Bodhidharma went to China to teach Buddhism, first of all he met Emperor Wu. Emperor Wu asked Bodhidharma, “I have built lots of Buddhist temples and educated Buddhist monks and nuns. What is the merit?” And Bodhidharma said, “No merit.”
> 
> Emperor Wu didn’t understand *no merit*, so he continued to [wonder], “If Buddhist teaching is no merit, why do we study Buddhist teaching?” It didn’t make sense to Emperor Wu, so he asked, “What is the essence of Buddha’s teaching?” Bodhidharma said, “Vastness; nothing.” The vastness of no holiness, and the vastness of nothing. 
> 
> This statement was very impressive, so although [Emperor Wu] didn’t understand, he felt something. So he continued [to ask]: “If there is nothing, and the essence of Buddhism is vastness of existence – if so, who are you?” Who is this little guy in front of Emperor Wu? And Bodhidharma said, “I don’t know.” Because even Bodhidharma is completely nothing holy, just vastness of existence. 
> 
> That *I don’t know* is not the usual meaning of “I don’t know” that you think. That *I don’t know* is that he knows pretty well, but still Buddha’s teaching is completely beyond the intellectual sense or intellectual explanation. 
> 
> So that is a very simple statement: “Nothing holy; just vastness.” But this is a very impressive statement. So from generation to generation, we still have to continue to think about this. It has been handed down from generation to generation because it is not merely words, it comes from Bodhidharma’s true heart. He really touches the core of existence. 
> 
> The core of existence is really silent – but pretty active. It’s very vast, because it is always embracing the whole thing. But according to human speculation, we think that is kind of contradictory, because [existence is] embracing everything in peace and harmony. So that’s why it’s vast, nothing holy; no discrimination there. 
>
> – From [“*Blue Cliff Record* Case 43: Tung Shan’s No Cold or Heat, Talk 1” (March 16, 1983)](https://katagiritranscripts.net/1983-03-16-Blue-Cliff-Record-Case-43-Talk-1)

This is what Bodhidharma came to China to transmit. 

--- 

After his meeting with Emperor Wu, legend says that Bodhidharma travelled to the north  and sat “facing the wall” for nine years. People often have the idea that Bodhidharma’s nine years of “facing the wall” was about making a point, or the pursuit of some new level of enlightenment. But what if it was about practice for it’s own sake? 

> **Question:** You brought up the story about Bodhidharma sitting and facing the wall for nine years. And I was talking to someone about this recently, and this person told me that the reason that Bodhidharma went and faced the wall for ten years was because Emperor Wu didn’t understand what he was saying so he banished him. 
> 
> **Katagiri Roshi:** *[Laughs.]*
> 
> **Questioner:** And I always thought that Bodhidharma chose to go and face the wall for nine years to sort of make a point. What’s your understanding about why he went?
> 
> **Katagiri Roshi:** *[Still laughing.]* Well, that is a story; human beings try to understand the stories, you know? So everyone understands in a different way from that same story. But the point is, I think Bodhidharma sitting for nine years at Shaolin Temple is to manifest his life and the Buddha’s teaching. 
> 
> **Questioner:** Okay, that’s it. 
> 
> **Katagiri Roshi:** That’s it. Wherever he may go. 
> 
> For instance, when I come to the United States, on the surface there are many different changes: I used to be in Los Angeles, San Francisco, and [now] here in Minneapolis. But strictly speaking, I’m always sitting and facing the wall. Nothing to teach you, actually. That’s all I have to do. And also, you have nothing to get from me. You’re always sitting facing the wall and being in the location I mentioned (where everything intersects). [...] Day to day, you have to take care of [life] in terms of that location, and then many, many different worlds are coming up, you know? San Francisco and Minneapolis. And then each time we have to take care of different pictures, but basically you have to be in the same location always. That is sitting for nine years; that’s the meaning of Bodhidharma sitting. 

--- 

And we sit facing the wall to this day. But here is some more information about what “facing the wall” actually means:

> In zazen we practice facing the wall. Bodhidharma [talks about] “wall meditation.” Wall meditation means facing the wall, [...] observation of the wall, looking at the wall. “Looking at the wall” doesn’t mean *you* look at the wall, okay? The wall is *emptiness*. The wall is the source of existence; [there is nothing] there. 
> 
> So doing zazen, facing the wall, means abiding firmly in zazen, right-now-right-here – and then, what can you experience? This is *emptiness*. Nothing. But *nothing* doesn’t mean nothing, because simultaneously [...] you can touch very deeply the source of the human phenomenal world. That’s why in the *Nirvana Sutra* [it says], “If you want to see suchness, the truth of the human world, you have to see it through meditation, zazen.” That’s why doing zazen is very important for us. 
> 
> – From [“Mindfulness – Talk 1” (March 21, 1984) at 1-26:16](https://katagiritranscripts.net/1984-03-21-Mindfulness-Talk-1#1-26:16)

Katagiri Roshi says that as part of facing the wall we must practice *deep faith*:

> Basically, first we have to establish a deep faith that all sentient beings have the-same-and-one-nature. And second, we have to establish a state of the mind that is like a wall, so-called emptiness. So that’s why you always [sit] “facing the wall.” The wall is [emptiness].
> 
> So first you have to have a very deep faith, that all sentient beings have the-same-and-one-nature. Whatever happens, whether you like or don’t like it, beyond this, everything exists just like that. That is a very deep faith. *Deep faith* means your life must stand up straight there. *How?* That is second. You have to establish the state of your mind that is like a wall, so-called emptiness. In other words, abiding firmly in a state non-dualistic understanding. 
> 
> – From [“Mindfulness – Talk 3” (March 23, 1984) at 1-36:20](https://katagiritranscripts.net/1984-03-23-Mindfulness-Talk-3#1-3620)

We will discuss this kind of faith more in the next chapter, Chapter 9: “Take the Backward Step.”

--- 

Katagiri Roshi comments on a line from a verse in *The Blue Cliff Record*:

> > Even Yellow Head (Buddha) and Blue Eyes (Bodhidharma) have yet to discern.  
> 
> Well, even Buddha Shakyamuni or Bodhidharma cannot understand it, cannot *know* what it is. But anyway Bodhidharma and Buddha Shakyamuni – or ancestors, your parents, your grandparents – continued to dwell in the beautiful life force of nature constantly, making their life mature, instead of *knowing* or *analyzing* constantly. [That] is a *part* of human activity, but it’s not all. 
> 
> So, it is not something to realize or to know, but to dwell in and make your life deepen or mature. That means that, here it says, “even Yellow Head (Buddha) and Blue Eyes (Bodhidharma) have yet to discern.” It’s not a matter of discussion. No. It is something you have to do. 
>
> – From [“*Blue Cliff Record* Case 51: Hsueh Feng’s What Is It? – Talk 2” (January 18, 1984) at 50:30](https://katagiritranscripts.net/1984-01-18-Blue-Cliff-Record-Case-51-Talk-2#5030)

So, how can we today dispense with wholehearted practice?

--- 

In Chapters 1 through 8, we’ve looked at the first part of *Fukanzazengi*, where Dōgen Zenji more or less talks about *why* we do zazen. Of course, really we’ve been talking about what zazen *is* all along. But basically, we can say that in Chapters 9 through 11 we will now look at Dōgen Zenji’s statement of *what* to do. And then in Chapters 12 through 25, we will look into details of *how* to do it.

```{=typst}
#pagebreak()
```

# Chapter 9: Take the Backward Step

## Paragraph 4 Part 1

> 所以須休尋言逐語之解行、須學回光返照之退歩。

> Therefore, put aside the intellectual practice of investigating words and chasing phrases, and learn to take the backward step that turns the light and shines it inward. [SZ] 

> You should therefore cease from practice based on intellectual understanding, pursuing words and following after speech, and learn the backward step that turns your light inwardly to illuminate your self. [EB] 

## Commentary

The first part of *Fukanzazengi*, which we discussed in Chapters 1 through 8, discusses *the Way* and *practice-realization*. We could say that the first part is explaining *why* we do zazen. Having established that, next is a direct statement of *what* we should do:

> You should therefore cease from practice based on intellectual understanding, pursuing words and following after speech, and learn the backward step that turns your light inwardly to illuminate your self. Body and mind of themselves will drop away, and your original face will be manifest. If you want to attain suchness, you should practice suchness without delay. [EB]

These three sentences are the subjects of Chapters 9, 10, and 11. 

---

We discussed in Chapter 4 and elsewhere that the teaching of Buddhism goes beyond the practice of intellectual understanding. What’s the alternative? We need to “learn to take the backward step that turns the light and shines it inward.” 

“Turn the light and shine it inward” is *ekō henshō* (回光返照), a key term in Zen Buddhism. To do that, we “take the backward step.” However, translations of this line vary a great deal, as do opinions about what it actually means.

Katagiri Roshi says:

> [...] “Learn the backward step” means, let’s return to that very inception of the moment. The very inception of time and space. The very inception of *gassho*, or zazen. In other words, just put yourself right in the midst of the inception of doing zazen, *gassho*, standing, et cetera. It means let’s go back to the original moment, the first moment. Again and again, again and again. 
> 
> And then, if you *do it*, even for a moment, it “turns your light inwardly to illuminate yourself.” Very naturally you create a wholesome world, a peaceful, harmonious world, even [if] you don’t see it. This is [that] naturally it’s going. 
> 
> So that’s why, if you continue to do it, naturally you will come to enhance or to deepen your life. Even though you don’t know how much your practice is progressing or not, it doesn’t matter. Sometimes you can see how much; sometimes you cannot see. *Most of* the time you don’t see how much your practice is making progress; no. But all you have to do is constantly go back to that source of being, existence. 
>
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986) at 44:03](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4#4403)

If we’re expecting this line in *Fukanzazengi* to be a kind of special technique or trick to “do meditation,” what follows in this chapter may be surprising, perhaps even frustrating. Because to “take the backward step” is something simple, *very* simple. In fact, we already covered it, in Chapter 7, “Playing in the Entranceway”:

> So how do you be free from this very minute vibration of the mind, from moment to moment? It’s very difficult to say *how* you do it. No, we don’t know. But this is the *tathāgata* stage, according to *The Awakening of Faith*. It is true! So finally, that is the place [where] the one world, where the very minute vibration of the mind can be realized: by buddha-*tathāgata*. At that time, buddha-*tathāgata* knows how to live there. 
> 
> Because whatever you think, no matter how long you cognize or you realize that very minute vibration of the mind, you never stop vibrating your mind. So how do you stop vibrating your mind? This is, it’s very simple, *very* simple. It’s very simple, but it’s too simple to know. *[He laughs.]* So all you have to do is just *be there*. 
> 
> Just be. *Tathāgata* stops vibrating. “*Tathāgata* knows how to stop vibrating” means just *be* exactly – with no second person, no second thought. This is total dynamic working. You become exactly one.
>
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986)](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4)

If you got that – or maybe even if you didn’t get it – this is probably a good point to pause, stop reading for a while, and maybe do some actual zazen, before continuing.

In the same talk, Katagiri Roshi says much more to explain this, so we will go back to the beginning and cover some ground. 

--- 

Katagiri Roshi’s teachings about “taking the backward step” take us in a direction we might not expect: understanding the nature of Buddhist *faith*, or *belief*. 

Often in English translations of Buddhist texts, words with Western religious connotations are used where no such meaning is intended, which causes considerable confusion. For example, the word “defiled” means something very different in Buddhism (at least in Zen Buddhism) than how it is usually heard. (In Buddhism, *defiled* means basically the same as “dualistic”; there is no moral implication, or at least far less of one.) So one might justifiably wonder, “Is there a translation issue here?”

“Faith,” however, is an accurate translation of the Sanskrit word *śraddhā*, in Japanese *shin* (信). Still, we have to be careful how we understand this faith. Buddhist faith is not so much faith in a religious figure or a doctrine. Buddhist faith is faith in the Way: “Where all beings exist in peace and harmony, prior to the germination of any subtle ideas.” (See Chapter 2: “The Way.”)

What does that mean? Katagiri Roshi says:

> Today I would like to talk about the key point of the practice in terms of *faith*.
> 
> In *Gakudō-yōjinshū*, “Points to Watch in Buddhist Training,” Number 9 (“The Need to Practice in Accordance with the Way”), Dōgen Zenji says:
> 
> > To study the Way is to try to become one with it – to forget even a trace of enlightenment. Those who would practice the Way should first of all believe in it. Those who believe in the Way should believe that they have been in the Way from the very beginning, subject to neither delusion, illusive thoughts, and confused ideas nor increase, decrease, and mistaken understanding. Engendering belief like this, clarify the Way and practice it accordingly – this is the essence of studying the Way.
> > 
> > (From *Zen Master Dōgen: An Introduction with Selected Writings*, translated by Yuho Yokoi with Daizen Victoria, page 57.)
> 
> So the essence of the practice, practicing the Way, is to believe that you are present right in the midst of the Way, “subject to neither delusion, illusive thoughts, and confused ideas nor increase, decrease, and mistaken understanding.” This is the first important point. 
>
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986)](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4)

This is called “belief” – but it’s not intellectual belief, or at least it’s not limited to intellectual belief. In fact it’s more or less the opposite of that: it’s precise oneness with what’s going on, “with no confusions, no perverted views, no increase or decrease, no misunderstanding.” Dōgen Zenji says, “Engendering belief like this, clarify the Way and practice it accordingly.”

Why do we need this belief? For at least two reasons. The first reason is that “to become one with the Way” – “to forget even a trace of enlightenment” – we cannot do that through the intellect. The only way to is to put ourselves directly there, again and again. The only way we can do that is through something we can call “faith” or “belief” – because it’s something we are *doing*, enacting, right in the midst of whatever we are thinking or feeling about it. 

This “putting ourselves directly there” is “taking the backward step.” So in this sense, taking the backward step is the application of faith.

Again, taking the backward step is to “return to the very inception of the moment.” Katagiri Roshi says:

> So in the very inception of being, here and now – in other words, in the very inception of birth – [it] is completely [beyond] questions. But in that realm of the world, you are creating your life, constantly. That’s why everyone has a great capability to create a world, life. 
> 
> Everyone has great capability to create the human world. Whichever [way] to go: bad, good, whichever. But if you realize that realm of the one world, [...] I think you cannot create an unwholesome world – because it is very pure, and because you can see all sentient beings living in peace and harmony. [...] You cannot do something wrong, you cannot hurt anybody, so very naturally you create a peaceful world. That is so-called *creative* life *with* all sentient beings. 
> 
> That is [why] first we have to *believe* [in ourselves, that we are] exactly present right in the midst of this Way.
>
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986) at 15:16](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4#1516)

Katagiri Roshi says much more about this in the talk – some of which we have already covered, for example in Chapter 5: “Free from Dust,” where we talked about karmic life not being separate from total dynamic working. But for now, we need to move on to Dōgen Zenji’s second point, where he says how we *get to* this faith. 

---

Katagiri Roshi continues with Dōgen Zenji’s second important point in *Gakudō-yōjinshū*, “Points to Watch in Buddhist Training,” Number 9 (“The Need to Practice in Accordance with the Way”):

> But next, in the process of reaching this one world – so-called *belief*, *faith* – Dōgen Zenji says there are two processes. One is, *cut off the root of discriminative thinking*. Second: *body and mind dropping off*. 
> 
> This is our practice. This is [the process] to reach that belief, one world, [that] you are present right in the midst of the Way, without any delusions, confusions, perverted views, mistakes. How can we reach there? That is first, we have to cut off the root of discriminative thinking. 
>
> I mentioned the root of discriminative thinking is very minute vibration of the mind. This is called *root*, the root of the discriminating mind. We are *always* discriminating. Even though I am talking about this with wholeheartedness, still I am discriminating! Right in the middle of talking, I am talking to myself simultaneously as I am talking to you: “Hey, Katagiri... you are pretty good.” *[He laughs.]* At that time [this is] very minute vibration of the mind. Or if you dance on the stage, you are completely devoting yourself into dance, but still your very minute vibration of the mind is poking into that perfect state of the dancing – and then thinking, evaluating, discriminating. Do you understand what I mean? This is called *root*, root of discriminating mind. 
> 
> So how can we reach [...] the oneness, so-called *faith*, Buddhist faith? To cut off that root means [you say], “Please... shut up. Just do it.” *[He laughs.]* That’s it. Don’t you think so? “Please keep your mouth shut, do it.” That’s all we have to do. 
> 
> For instance, I mentioned maybe before, a gentleman in Japan was interested in running a business, so he asked a Zen master, “I have a big problem, please help me.” So the Zen master asked, “What’s that?” And then [the gentleman] said, “I am very interested in running a business.” Well, whatever kind of business, business is all right. But he was interested in running a business, and the teacher said, “Oh, that’s interesting. Please do it.” But the gentleman said, “I don’t have any money.” And then the Zen master said, “If you don’t have money, how can you run a business?” You cannot run a business, so stop and forget it. You know, stop running the business! *[He laughs.]* Stop thinking of running the business. [But the gentleman] says, “That is my problem, because that’s why I want to run a business.” And then the Zen master says, “How can I help you? That’s *your* business, not my business.” *[He laughs, and a couple people laugh.]* 
> 
> Is that clear for you? That is *cut off the root of discriminating mind*. Not ignoring discriminating mind. We are always doing [something] like this. “I want to do zazen, but I don’t want to have physical pain, et cetera. And I want to sleep in bed until 10 o’clock. So I want to do zazen, I want to deepen my life, et cetera; I want to be happy. But I don’t want to do zazen getting up in the morning!” *[He laughs.]* That is your problem. How can I help you? I don’t know; that’s your business! *[He laughs.]* Do you understand? 
> 
> That’s why, if you want to reach *tathāgata* stage, all you can do is, “Please keep your mouth shut. Just do it.” That’s all you can do.
> 
> But students are always depending on the teaching: “Please help me.” Well, yes, I can help you. But you should know that there is something in the realm of vibrating your mind very minutely – at that time there is nothing for me to do. So all you have to do is you just be in the *tathāgata* stage. That’s it. How? Cut off the root of the discriminating mind. 
> 
> You want to keep smoking? Yes, you want to, but it’s not good for you; the cigarette case always says it’s not good for your health. So you don’t want to keep smoking, but you cannot stop it. So [you say,] “This is my problem, please help me.” How can I help? That is always what we do.
> 
> So this is the best way, very simple, and *you* have to do it. I can help, and also ancestors and buddhas can help. But this is [that] the ancestors and buddhas always back you up; they are always behind you, encouraging you. Finally what you have to do is to do it *by yourself*. 
> 
> So this is the first point: you have [...] to reach that faith. Believing in yourself right in the midst of the Way, which is completely peaceful, harmonious – with all sentient beings. You should trust in *you* like this, and believe in *you* like this. 
> 
> [...] How can we do it? How can we reach there? That is the practice. First, cut off delusion, the root of discriminating mind. And then very naturally, secondly, Dōgen Zenji says, body and mind [are] dropping off. [...] This is called *total realization*. If you cut off the root of discriminating mind, put yourself right there, and then you can see the whole situation of the Twin Cities [as] if you are on the top of the IDS tower. 
> 
> But we always have a problem: I want to see the state of the whole situation of the Twin Cities area, but I don’t want to go [to the top of the IDS tower], you know? You want to see, but you don’t want to go. So how can I help? Nothing. So all you have to do is: go. That’s it.
> 
> So that is, if you put your body *right there*, then you can drop off your body and mind, you can be free from the root of discriminating mind. That means you can be exactly one with the very minute vibration of the mind. And then, no concept of the minute vibration of the mind.
> 
> So constantly you put your body and mind right in the middle of the very minute vibration of the mind, there. This is a very important practice. Constantly you have put your body there, put your body there, next moment, next moment, again and again.
>
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986) at 25:23](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4#2523)

People may have a reaction to hearing “please shut up.” In the next talk, there is a question about this:

> **Question:** Hojo-san? Taking the backward step, it’s like saying, “please shut up”?
> 
> **Katagiri Roshi:** *[Chuckles.]* Uh-huh. 
> 
> *[Laughter.]*
> 
> You don’t like it? *[He chuckles.]*
> 
> Well, even if you don’t like it, that is a final thing you can do; a unique, final thing you can do... after struggling for a long time. *[He laughs.]*
> 
> So that is a unique way to allow you to exist fully. 
>
> – From [“Principles of Practice, Talk 5: Direct Transmission” (March 23, 1986) at 1:03:30](https://katagiritranscripts.net/1986-03-23-Principles-of-Practice-Talk-5#10330)

This is the other reason why we need faith: because no-one can do this practice for us. Teachers can show and encourage us, buddhas and bodhisattvas support us, but the only person who can do *your* practice is *you*. So we have to have faith in ourselves: faith that we are already a “container” of the dharma, so we are completely qualified to do this practice. *Faith* is the motive power to actually do the practice. 

---

Katagiri Roshi continues:

> Anyway, let’s go back, let’s go back, every day. And then that is called *the backward step*. [It is] not “withdraw.” 
>
> That is called *reflection*. 

Interestingly, Katagiri Roshi calls the backward step “reflection.” This seems to mean looking deeply at discriminating mind in order to cut off discriminating mind. Why is this interesting? Because, in Buddhist terms, the movement of discriminating mind is *suffering*. 

*Suffering* (Pali: *dukkha*) is another deep topic in Buddhism. Katagiri Roshi goes into detail introducing “reflection,” “suffering,” and its root in “ignorance” (Sanskrit: *avidyā*, another key term in Buddhism) in [“Principles of Practice, Talk 3: High Resolve” (March 21, 1986)](https://katagiritranscripts.net/1986-03-21-Principles-of-Practice-Talk-3). Here, we need to stay focused on the backward step. But we should be prepared, once again, for the Zen understanding of these terms to be different from what we might be expecting.

In saying that the backward step is reflection, Katagiri Roshi is saying that our practice, constantly going back to the source of being,  involves suffering:

> [...] This reflection is [and] begets suffering; [it’s] really suffering. But that suffering is completely beyond your intellectual understanding; [it’s] before your intellect is suffering. Because everyone has to go back to there: consciously or unconsciously, the root of your being is coming from that realm. So very naturally, everyone always goes back to there, consciously or unconsciously. 
> 
> But most people don’t realize it! Even though they are standing there, they don’t realize it. But they are very interested in the world *after*: the second moment, second thought, third thought. That is the so-called *samsaric world*. That’s why the problem is going on and on; there is no peace. The more they try to get the peace, the more they beget not-peace in order to get the peace. That is *samsara*. 
> 
> That’s why if you want to be peaceful, please go back to the source of the first moment of the peace you have thought. Let’s go back. This is the backward step. The backward step is not escaping from. Anyway, let’s go back to that first moment of peace you have thought. 
> 
> In other words, cutting off the root of discriminating mind, be peace *right now*. Right now, with your whole body and mind. And that is immediately you create peace, peaceful world. 
> 
> But it is [an] event which occurs just in a moment, so you don’t see it. That’s why very naturally according to your intellectual sense, you can see “no hit” among a hundred thousand attempts to try to hit the bullseye. Nothing. That’s why we need the encouragement – “please, follow like this” – [which] Dōgen mentions. 
> 
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986) at 44:03](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4#4403)

We need encouragement because looking deeply at suffering involves... well, suffering. 

--- 

To explain further, Katagiri Roshi again turns to Avalokiteshvara:

> That is called *reflection*. And also Dōgen Zenji mentions in this book – Number Six (“Advice for the Practice of Zen”), page 53, the second paragraph from the bottom:
> 
> > The Buddha Sakyamuni said, “Turning the sound-perceiving stream of the mind inward, forsake knowing and being known.” 
> > 
> > (From *Zen Master Dōgen: An Introduction with Selected Writings*, translated by Yuho Yokoi with Daizen Victoria.)
> 
> This is cutting off the root of discriminating mind, so-called reflection. “Learn the backward step, and turn your light inwardly to illuminate yourself.” How do you do this? This is “Avalokiteshvara turns the sound-perceiving.” 
> 
> Avalokiteshvara is a bodhisattva who listens to the sound of perfect observation of the world. By means of observing very closely what the human world is, what human beings are, then he [or she] can listen to the kind of sound, very deep sound – in other words, very minute vibration of the world and of the human beings. Very deep. That is called *suffering*. 
> 
> Suffering is completely beyond your consciousness; it’s there. Because constantly we are returning to the source, returning to the source, even though you don’t know. So very naturally people are struggling for their life. Why do they struggle for their life? Because they want to get the something very deep, beyond consciousness or unconsciousness. That is they try to get that first moment of being present *right now, right here*. Where two worlds make one: intellect, spiritual world. This is this partition.
> 
> So, constantly there. Constantly we want to get it! But this is so-called reflection. Whatever we do, always we reflect upon ourselves. “Are you sure? Are you sure? Are you are happy? Yes, you are happy. But are you sure?” Constantly you ask yourself, and then try to get something which makes it possible for your happiness to *be*. Still you want. Because this is to try to come back to the source, naturally. This is *suffering*, so-called. 
> 
> So does suffering come from your intellect or your six senses? No. Completely beyond. That’s why [it’s a] “noble truth” – suffering is noble truth. So suffering is pretty deep. 
> 
> So Avalokiteshvara listens to that sound. If you listen to the sound, immediately you are caught by the sound which you can hear, and also the sound known by human beings, [or] Avalokiteshvara. It’s already subject and object. So we are already washed away by the sound-perceiving stream of mind – that means the six senses world, created by the six sense organs. We can hear, immediately we create six senses world. That is *samsara*. Then, naturally, most of us are completely washed away by this six senses world. Whatever you listen to or whatever you know – good or bad, wholesome, unwholesome, whatever – we always [are] carried away. We always are discriminating. 
> 
> So very naturally Avalokiteshvara listens, but simultaneously Avalokiteshvara is free from knowing and [what] is known. Free from subject, object. It means Avalokiteshvara constantly stands up in the *source*, [the] first source, the very basis of the being, which is silent and stable, from where the life of all sentient beings blooms. So Avalokiteshvara constantly goes back to that space, that world, that point. And then, he or she can help. He or she can help all sentient beings. 
> 
> So that is called “Avalokiteshvara turns the sound-perceiving stream of the mind, forsakes knowing and being known.” According to Dōgen’s message, I think you have to cut off the root of discriminating mind. 
> 
> [You may ask,] “Shall I do zazen forever, in order to deepen my life, in order to make my life happy?” Yes, you should do it. 
> 
> But you don’t want to [have] the physical pain, and you don’t want to get up early in the morning, et cetera. So, well... if you don’t want, please, don’t do zazen. 
> 
> But still you want. If you want, please come. But you don’t want. Always back and forth, back and forth. How can I help? 
> 
> So all you have to do is, you have to forsake knowing and being known, “shall I” or “shall I not.” You just be. At that time, you are a really great person, so-called Avalokiteshvara Bodhisattva, who can have a really willing ear to listen to the sound of the world, the sound of you. And then, you can help. This is *compassion*. 
> 
> So, this is the point of the practice in terms of Buddhist faith. 
> 
> Constantly, first of all, you are a great container [of dharma]. Trust in this: you are a great container, beyond good or bad, right or wrong. Don’t put yourself down, don’t despise yourself. Anyway, encourage yourself constantly, and do it. 
> 
> That’s why Dōgen Zenji says practice is just like walking in the mist. It’s a really good example: walking in the mist, constantly, and then, before you are conscious of it, your dress gets wet. This is our practice. Otherwise, you cannot continue to practice, no. It’s very difficult to build up peaceful world. But if your practice is exactly just like walking in the mist: before you are conscious of it, your dress gets wet. If you practice like this, you really create peaceful life. And you can help all sentient beings. 
> 
> – From [“Principles of Practice, Talk 4: Faith” (March 22, 1986) at 55:14](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4#5514)

--- 

In the next talk, Katagiri Roshi says even more to clarify the nature of *reflection* and *suffering*. In general we don’t like suffering, but because of suffering, we can live, and we can practice:
 
> *Zazen* is to “manage free practice and realization.”
>
> Yesterday I [talked] about the practice. The practice is constantly you have to come back to the beginning, the very beginning of your existence. You come back to the very beginning of your birth, come back to the very beginning of standing, right now, right here. The very beginning. [It’s] not to come back to the result which you can see. Standing, [for example,] is not a result. You have to come back to the *real* source of standing right now, right here. And then, this is real managing zazen.
> 
> What is this? When you come back to the real source, that is called “managing free practice and realization.” Because when you come back [to] that source, this is pretty hard, pretty hard practice. So it’s practice! Because we are already creating our own life, and then we have to put it aside and go back to that *one*, that source. That’s pretty hard practice. But when you go back to there, it’s not hard practice! Immediately you are supported. 
> 
> Just like jumping into the ocean. Before you jump into the ocean, you have to think what the ocean is, what swimming is, what the fear is. I don’t know what happens in my body and mind; maybe the moment when I jump into the ocean, I could die. I don’t know; there is no guarantee. So, lots of stuff is coming up. That’s pretty hard practice: training your body, your mind; understanding swimming, oceans, and the form of swimming, et cetera. But [...] the moment when you jump into the ocean, simultaneously your body floats. Very naturally, you are supported. 
> 
> So, this is what is called “to learn the backward step which turns your light inwardly to illuminate yourself.” *Fukanzazengi* says this. Or, plainly speaking, it is called *reflection*. 
> 
> So, in a sense, *reflection* is considered as human suffering beyond human consciousness. [It’s considered] in terms of hard practice. It’s really hard practice, because suffering is really a serious matter in life. [...] Because you cannot get out from this. 
> 
> But [because of] this suffering, you can survive! You have to appreciate this suffering, because we are seeking constantly for something more than the conscious world or unconscious world. We are seeking for it, *always*. This is the suffering. That suffering comes into existence beyond the functioning of your consciousness, so it is very serious in life. But if you realize that suffering – real suffering coming from the first moment of your being, exactly – then you can attain enlightenment. So, suffering makes you sad and painful, but on the other hand, suffering makes you become big laughter, relief. You can [be relieved], exactly. 
>
> Well, you can experience this in your life. If you cry day [after] day, one moment completely crying [turns into] big laughter. Just like the bottom of a bucket broken and the water rushing away from it, all of a sudden. 
> 
> So, this is the real picture of human suffering. 
> 
> – From [“Principles of Practice, Talk 5: Direct Transmission” (March 23, 1986) at 28:28](https://katagiritranscripts.net/1986-03-23-Principles-of-Practice-Talk-5#2828)
 
 --- 

Sometimes “take the backward step” or “turn the light around and shine it back” (*ekō henshō*) are understood as meaning to focus “internally” on ourselves, shutting out the “external” world. It is indeed sometimes described as “coming back to oneself,” but we have to be careful in how we understand this. A good example is found in one of Katagiri Roshi’s talks on *Blue Cliff Record* Case 52. He talks about “going out” and “coming back”:

> So in our daily life, we are always getting something. To get something means to make a choice of direction, simultaneously, you can get [something]. But to get something means to throw [away] that [other] one. [That] means you negate the present.
> 
> To negate your present means “to go out.” Do you understand? To go out – so you never have a chance to come back to you, and settle down, settle yourself in the self, and be stable. You never do it. If you continually try to fill up the satisfaction, looking for a direction with the affective preferences, always there is uneasiness, and madness, lots of madness there. So that’s why it’s pretty hard for us to participate in ourselves *directly*.

But later in the same talk, Katagiri Roshi seems to slip into speaking about “internally” and “externally,” and quickly corrects himself:

> Let’s participate in ourselves internally... [no,] not “internally”. If I say “internally,” simultaneously “externally” is there. *[He laughs.]* So, beyond internally or externally, participate *in you*, and learn *you* as you are, directly. Not imaginary, not turning toward, not with affective preference – constantly you do it.
> 
> Because your existence is *yours*. Just like the trees [in the mountains covered with snow]. But not yours! There is a huge vastness of existence, life force there, life energy there – behind you, or inside you. One tree, your tree, teaches you the name of the tree – your body, your name. But simultaneously the rhythm of the vastness of existence is there.
> 
> That is you. So you have to participate in that.
> 
> – From [“*Blue Cliff Record* Case 52: Chao Chou Lets Asses Cross, Lets Horses Cross – Talk 1” (January 21, 1984) at 1:09:44](https://katagiritranscripts.net/1984-01-21-Blue-Cliff-Record-Case-52-Talk-1#10944)

This may be why Katagiri Roshi clarifies that the backward step is “not [to] withdraw” and also “not escaping from.” 

--- 

In Zen, an *eko* is the dedication we do after a ceremony or any activity. As Katagiri Roshi says, “*Eko* is turning the merit to all beings, instead of holding on to it by yourself.” Katagiri Roshi connects this *eko* (回向) with *ekō henshō* (回光返照), “turning
the light and shining it inward.” In a talk on *karma*, he translates this line from *Fukanzazengi* as “to learn that one withdraws one step and turns the light inward on oneself.” But “withdraw one step” still does not mean “escape”:

> ... in Zen Buddhism particularly, Dōgen Zenji says it another [way, in *Fukanzazengi*]. He says, “To learn that one withdraws one step, and turns the light inward on oneself.” *To withdraw one step* doesn’t mean to escape from something. To withdraw means not to attach to what you have done, [but be] aware of what you have done. Whatever good or bad, don’t [attach to] it, don’t be crazy about it. It doesn’t mean you should ignore it, but you should awaken to what you have done. That is “to withdraw one step.” And then, if you do something good, withdraw one step and “turn the light” – [*the light*] means *merit* – “inward on oneself”: *inward* means wisdom, *on oneself* means oneself and another, all beings. Anyway, *share* life, or merit. Give life, or light, coming from what you have done, to everybody. That [is the meaning of] “to learn that one withdraws one step and turns the light inward on oneself.” At Eiheiji Monastery, in the entrance of the study room, a handscroll there says [this]. This is the attitude toward studying the Buddha Way. 

An obvious question here is how “inward” means “wisdom,” and how turning merit “on oneself” means “on all beings.” The answer is probably that this “oneself” is oneself in the sense of “your original face,” which is what manifests when we take the backward step. 

Later in the same talk, he mentions this specifically in terms of karma: 

> So very naturally, you can see your life not only in terms of manifested karma, but also unmanifested karma, which manifested karma is backed by. So very naturally you can see your life extending to the beginningless past and endless future. This is called *eko*, or *virtuous quality*, or “learn that one withdraws one step and turns the light inward on oneself.” Very naturally that means that you can learn humility, and modesty, compassion, toward oneself and another. 
> 
> – From [“Karma: Karmic Retribution in Present Life” (July 10, 1980) at 50:45](https://katagiritranscripts.net/1980-07-10-Karmic-Retribution-in-Present-Life#5045)

In other words, “turning the light around” is the same as turning the light to benefit all beings. 

This connection is mentioned in the first talk in the *Fukanzazengi* (1979) series:
 
> How can you experience enlightenment? Well, first: practice egolessness. How can you practice egolessness? *Samadhi*; one-pointedness. And then, just do it. And then if you just do it, there is no design on expecting any reward. Just do it. That is *shikantaza*. 
> 
> That is really helpful. That is really a way of helping people: offering your merit, the merit of your practice, to all sentient beings. 
>
> – From [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 1” (June 9, 1979) at 56:36](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1#5636)

--- 

Indeed, learning to “take the backward step that turns the light and shines it inward” is not self-centered – and although we are discussing *zazen* here, it is also not limited to zazen. We discussed that the backward step is *reflection*, which involves deep contemplation of *suffering*. Katagiri Roshi connects this practice to the Buddhist *pāramitās*, including the Precepts:

> What we can do is, constantly cultivate this practice. Be in the realm of first thought, and practice there, and then simultaneously you can get the wisdom and its functioning, which is called *root of the wholesome*. 
> 
> You never lose it, because wisdom and the functioning of wisdom is already planted in the bottom of your life. So, you never lose [it], whatever happens, all circumstances. That’s why, next moment, you can live in the Buddha land. How can we be free from karmic life? Well, just be there and practice. Very naturally, you are free. Exactly.
> 
> But our consciousness doesn’t believe it. *[He laughs.]* Because consciousness is already involved in the very complicated world, so we don’t believe it. But if you make your mind very clear and simple, going to the bottom of that reflection and discriminating world, then you can see how the first thought is working. And then, this is a really great light of instruction, how to live. All we have to do is to be there and practice, as best as we can. This is called *egolessness*. 
> 
> So, very naturally, suffering begets selflessness. Okay? Suffering. Because suffering is fabricated [by] reflection and discriminating mind, and simultaneously it is constant unconscious effort, which allows you to go on and on, [to know] the bottom of the samsaric world. So, very naturally, you can see how to live, how to take care of the samsaric world. 
> 
> So, let’s go down to the bottom, and then be there, and try to live. 
> 
> But still, in the samsaric world it is very difficult. That’s why there are several skillful methods: so-called six *pāramitās*. Let’s follow this way. 
>
> ... So, *giving*. Constantly giving. This giving is not the usual giving; [it is] giving *pāramitā*. *Pāramitā* means “perfect accomplishment.” So, giving must be accomplished perfectly. That means, completely open, and just do it. 
> 
> And also *precepts*. Precepts are Buddha’s suggestion how to live. Buddha’s suggestions – not moral suggestions, not ethical suggestions, *Buddha’s* suggestions. The suggestion of the truth, how to live. 
> 
> And also *effort*, and *patience*. And also *wisdom* and *dhyana* (meditation). 
> 
> Let’s do this. And then, very naturally, we can come back to the source of *samsara*. 
> 
> So that’s why mindfulness is pretty important for us. Let’s come back. *Mindfulness* [means] constantly remember. You must remember not only with a thought, but you must remember that first thought of *samsara* with the whole body and mind. That’s why you can come back. And then, you can be in *dhyana*, so-called meditation, or *samādhi*. You can be there. 
> 
> That is the practice of egolessness. So that’s why Buddha says, “Suffering begets selflessness.” Egolessness. 
> 
> – From [“Principles of Practice, Talk 3: High Resolve” (March 21, 1986) at 35:11](https://katagiritranscripts.net/1986-03-21-Principles-of-Practice-Talk-3#3511)

So we can see that zazen and the Precepts are closely related.

---

Far from withdrawing or escaping from life, “the backward step” is closely related to *prajñā*, or *wisdom*. Here Katagiri Roshi says that the *essence* of prajñā is “originally pure and clean” – we could say “perfect and all-pervading.” And the *function* of prajñā is “the backward step”:

> I think *prajñā* can be considered in terms of three points. 
> 
> One point is the *essence* of prajñā, the essence of wisdom. The essence of wisdom is [that] the self nature is originally pure and clean. This is the essence of *prajñāpāramitā*.
> 
> And the *function* of prajñāpāramitā is... how can I say it. In *Fukanzazengi,* Dōgen Zenji [says], “Learn the backward step that turns your light inwardly to illuminate yourself.” This is the *function* of the prajñā. 
> 
> [...] The essence of prajñā is [that] the self nature is originally clean and pure, that’s why if wisdom works, [there is] nothing to bring in from outside. You have [it] already. So if you return to the original nature of existence, it simultaneously illuminates. If you come back, *you* illuminate. In other words, if you come back to *original nature of existence*, you can experience religious transformation at 360 degrees: exactly turn [around]. That is *illuminate*.
> 
> So no one helps you; you have to do it. If you practice sincerely, more or less everyone experiences this [...] 180 degree or 360 degree turn-[around]. 
> 
> Well, there are many kinds of experience. Some experience this very slowly, very slowly. And some experience a *little* shock. Some experience nothing, but it’s penetrating, soaking through just like rain soaking through the ceiling, something like that. So they don’t realize, but it’s soaking through. 
> 
> Some experience a *big* shock, you know? Like thunder, lightning, exactly. Zen teaching is always talking about such experience, fascinating experience. But not everyone [experiences this], okay? 
> 
> So, many kinds of experience. But more or less, people can turn over their lives 180 degrees, if you really come back to original nature. That is how; this is [the] zazen we do. That is [the] “turn your light inwardly to illuminate yourself” that Dōgen Zenji mentions in [*Fukanzazengi*]. Is that clear?
>
> – From [“*Platform Sutra* – Talk 2” (March 20, 1987) at 3:26](https://katagiritranscripts.net/1987-03-20-Platform-Sutra-Talk-2#326).

 “Turning the light around to shine within” immediately leads to the next line: “Body and mind of themselves will drop away, and your original face will manifest.” Which brings us to the next chapter.

```{=typst}
#pagebreak()
```

# Chapter 10: Body and Mind Will Drop Away

## Paragraph 4 Part 2

> 身心自然脱落、本來面目現前。

> Body and mind of themselves will drop away, and your original face will manifest. [SZ]

> Body and mind of themselves will drop away, and your original face will be manifest. [EB]

## Commentary

One of Dōgen’s most well-known and frequently used terms, coming from his teacher Rujing, is “casting off body and mind,” or *shinjin datsuraku* (身心脱落). Here the expression is slightly different: “Body and mind of themselves will drop away” (身心自然脱落). This happens naturally in response to “taking the backward step that turns the light inward,” which we discussed in the previous chapter.


“Body and mind of themselves will drop away” is extensively discussed in the Katagiri Roshi's [series of talks on *Fukanzazengi*](https://katagiritranscripts.net/fukanzazengi). Particularly see the beginning of [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 4”](https://katagiritranscripts.net/1979-06-12-Fukanzazengi-Talk-4): “In shikantaza, all delusions drop off from the first. That is dropping off body and mind, body and mind dropping off. That is zazen itself.” And also: “Dōgen Zenji says, ‘Zazen is dropping off body and mind.’ Remember this. In your whole life, you should remember: ‘Zazen is dropping off body and mind.’ It means all delusions drop off.” 

- so here we see that “dropping off body and mind” and “dullness and distraction are struck aside” mean the same thing. 



 [“Principles of Practice, Talk 4: Faith”](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4): 
But next, in the process of reaching this one world – so-called *belief*, *faith* – Dōgen Zenji says there are two processes. One is, *cut off the root of discriminative thinking*. Second, *body and mind dropping off*. 


The specific term *shinjin datsuraku* is discussed in  [“Zazen: Dropping Off Body and Mind”](https://katagiritranscripts.net/1987-01-24-Zazen-Dropping-Off-Body-and-Mind) and in [“Zazen: Entry to the Buddha Dharma”](https://katagiritranscripts.net/1987-03-07-Zazen-Entry-to-the-Buddha-Dharma). In particular, [“Zazen: Dropping Off Body and Mind”](https://katagiritranscripts.net/1987-01-24-Zazen-Dropping-Off-Body-and-Mind) is an important talk where dropping off body and mind is discussed in relation to *compassion*.

On “ah”:

Let me say [more about] this. What do [we] mean by “dropping off body and mind the moment when you do zazen, the moment when you devote yourself in zazen”? Let me say it like this. 

[...] Let’s imagine that you [are getting into] a hot bath in the cold weather. In the rigors of Minnesota winter, your body becomes very cold. After that, you put your body right in the middle of a hot bath, okay? The moment when you put your body and mind in the hot bathtub, what do you say?

> **Several people:** “Ah.”
> 
> **Katagiri Roshi:** “Ah!” *[Laughter.]* 
> 
> That’s pretty simple! “Ah!” – that’s it. It’s no particular word, [just] a simple word. “Simple word” means a ground word, coming from the bottom of your heart. When your body and mind becomes one with the hot water and bathtub and all circumstances – including your memories, and distractions, dullness, all stuff. And then when you become completely one with the [bath], then you can demonstrate simplicity in life – so-called, “Ah!” That’s it. 
> 
> Within the “ah” – who are they? Can you pick up something particular? Pay attention to just the moment, at the very moment when you say “Ah.” *Who* are they? What is it? What is there? Can you say it? 
> 
> *After* “ah,” you pick up *you*, who says “ah.” But I am talking about *before* you say “ah.” Okay? 
> 
> Here is a partition, a very thin partition, just like a very thin curtain. Very thin silk. Not silk... silk is still touchable, but that partition is not touchable, but it’s still something there. Just like a mist. A mist is pretty hard to grasp, but it’s there. And then if you touch it, it disappears, and you can get next door. This is a [...] door. 
> 
> So [...] you are coming back to your home, and you put your body and mind in the bathtub. And then immediately within this partition you create your own life, so-called “ah.” Simple life. And then right before this partition, right before you touch [it] – this is the very beginning of the moment, okay? The very moment, before you think of it, before something runs through your consciousness. In that [situation], I think your body and your consciousness and the water become exactly one. That situation is never described. But your body and the water [are] functioning simultaneously, together.
> 
> And then, the next moment, you say, “Ah.” That is the next moment. And then when you say “ah,” people are very interested in the “ah” which you have demonstrated. Then, you are involved so much in what “ah” means. *[Laughter.]* What are they – the hot water, and your body and mind? Who makes me say “ah”? Something like that. This is “scientific,” you know? Modern civilization. And then finally, you don’t know where you are going. And also, you completely forget the first stage, the very first stage of your life. Completely you forget. 
> 
> [In the] first stage of your life, there are many beings which are functioning interpenetratedly, interconnectedly, together. This is *oneness*. Look at this sunny, wonderful day, you know? Well, how many beings exist? When you feel that wonderful sunny day, you say, “Ah, wonderful!” And before you say “wonderful,” how many beings are working together, interpenetratedly, without any hindrances? This is called *the universe*, we say; this is called *oneness*. In the oneness, that is a place where all beings come together and are working together and walking hand in hand, without hindrances, creating a peaceful world. 
> 
> Even [beyond] Minnesota. The rigors of Minnesota winter shake hands with the winter of Hawaii, in peace. You don’t believe it, but this is true. The Japanese monkey talks peacefully with the elephant in India. Can you believe it? You don’t believe it. But this is the place where all sentient beings come together and talk together, which is called *oneness*. We say *universe*, we say the *truth*. 
> 
> But if you are involved so much in the dualistic world, *after* creating a “wow,” you completely forget that first stage of your life. That’s why spiritual life is constantly to let you [get] back to the first stage, the first stage of a “wow.” That’s it. 
> 
> That’s why you don’t understand it. But when you are there, completely the dullness and distraction, the form of the five *skandhas*, are struck aside from the beginning. And then, what do we mean? Your body and hot water becomes one. This is called *intimacy*, perfect intimacy. *Secret* intimacy we say: very secret intimacy. No gap between. 
> 
> This is called *right*, [this is] the meaning of the *right*. And also that is a gate, entrance, to communicate with the universe. *Universe* means the total picture of your life working together with all sentient beings. Okay?
> 
> So that is called *dropping off body and mind*. When you do zazen, immediately you say “Ah!” That’s it. But you don’t say “ah,” because zazen has no particular object, so-called *bathtub*, you know? So that’s why you don’t know. You are always using your mind and body, and that’s it. That is subjectivity and also object. And then the whole world comes into you. 
> 
> And then, when you say “Wow!” this is called *samadhi*, we say. *Concentration*. Total concentration, total devotion. And also this is called *jijuyu samadhi*, “self-joyousness.” *Self-joyous samadhi*, we call it. 
> 
> In other words, this is called, “Ah!” That’s it. But in zazen, you cannot say “ah,” because everyone [is] quiet. *[There are some chuckles.]* So, you have to enjoy the self-joyous samadhi concentration right in the middle of zazen.
> 
> This is “dropping off body and mind.” 




> And then if you go back to that source, you don’t know what it is, but there is really a kind of astonishment, enormous astonishment. 
> 
> And then from this astonishment, you can build up philosophy, psychology – Buddha’s teaching. What is the beginning of the teaching – philosophy, and psychology, Buddhism? It is just astonishment, just surprise. 
> 
> That surprise is described as the Buddha land, [in a] literary sense. You know, the beautiful Buddha land is coming up, adorned with various seven jewels, et cetera. Very naturally you can build up a wonderful world, because it is just astonishment. Nothing to pin down. But directly you can feel it, you can touch it. Something touches your heart. 
> 
> So just surprise; *big* surprise. Then from this big surprise, the human world is coming up, and philosophy is coming up. *Physics* is coming up. Buddhism is coming up, Christianity is coming up. God, [and] any ideas are coming up from this. So finally what you have to do is, let’s go back to that simple and silent and clear world. So-called “just surprise,” huge surprise. 
> 
> Just like facing the moose when you drive in the countryside, as I mentioned. Exactly that [example]. “Wow!” – that’s it. When you say “Wow!”... [and] next moment: “A moose!” – it’s too late. *[He laughs.]* When you really face the moose and the whole world, it’s just a surprise. So, just *wow*. And then, the whole world is coming up from this: Katagiri, cars, and countryside, wilderness, and animals, and also trees, birds, insects. The whole world is coming up. And then we can create a poem from that. And we can create physics from that world. How the moose is connected with nature, you know? And including me, including modern civilization, so-called car. Anyway, it’s connected, so you can create physics, you can create psychology, you can create philosophy, you can create spiritual life. 
> 
> So it’s very simple, a very simple world. But it’s really huge, you know, the shock for you. That’s so-called spiritual life. It’s really spiritual life. 
> 
> So the purpose of spiritual life [is], simply speaking, you should touch this enormous surprise. That’s it. 
> 
> Well, if you explain what it is, it is simple, very simple, and clear, and silent. But simultaneously, the whole world is coming up. That’s why Dōgen Zenji constantly says in *Shōbōgenzō*, “Self is the whole universe.” The mountains, rivers, pebbles, are all sentient beings. All are buddhas. The whole world is coming up. 
> 
> But that whole world coming up [is] very simple situations. That is first thought, we can [confront] it with. This is the egolessness. We have to practice this. 
> 
> 

It is basically the same as “flow experience.”

> Nyojo Zenji (Tiantong Rujing), Dōgen Zenji's teacher, [said] that “*sanzen* is *zazen*,” [and] zazen is *shinjin datsuraku*, “body and mind casting off” or “casting off body and mind.” [...] This is the key point of our practice of meditation, the Zen meditation we do. So today I would like to say [something] about this.
> 
> First of all, you should keep in mind that Zen Buddhism tries to see or hear or understand the world and human life in terms of practice, or [...] action. Or *action* is still a concept, so I would like to say, “the point of action which is constantly going.” So, *flow action*, or *flowing activities*.
> 
> Zen Buddhism, particularly Dōgen Zenji, constantly mentions that we should see or hear [or] understand the human world in terms of flow actions, flow practice, flow process. Constantly, under all circumstances. Not in terms of *concept*, not in terms of the conceptualized world. The world you can usually see is already something conceptualized; this is the world you live [in] and you believe. But if we present the world [as] something more than conceptualization, you are very confused, because there is nothing to depend on. 
> 
> Usually everyone depends on, consciously or unconsciously, conceptualization of the world. That's it; that is your world. So the Buddha and ancestors try to present the world *before* you conceptualize. That's why it is a little difficult to understand it. But, we *have* to. We have to research it. We have to *taste* it. We have to understand it. Okay? 



> So [as I mentioned], Zen Buddhism tries to see or hear [or] understand the world in terms of the flow process, flow activity, flow action – not in terms of conceptualization. 
> 
> Of course, conceptualization is important, because we live already in the world conceptualized by us. The world of conceptualization is kind of a blueprint you can draw. It's important for us. Through the blueprint, you can imagine what the house will be, and you can build up practically what kind of a house it should be. So a blueprint is important, [so that] you can imagine, you can be a person who can build. You can be a carpenter. You can be the person who looks at, who imagines objectively what kind of house will be. But [...] blueprint is blueprint, so you cannot *live* there, [in the blueprint]. Is that clear? 
> 
> In the world of conceptualization, I think people become, what would you say... onlookers or carpenters. You become an onlooker or you become a carpenter. *Carpenter* means you participate in building up a house directly. [...] *Onlooker* means I am not a carpenter; so I can look at the blueprint, and through the blueprint I can imagine what kind of house will be, but [...] I don't understand what kind of house will be through the blueprint. But I have a right to look at the blueprint... constantly *[he laughs]*, with hope and desires. So always looking at [the blueprint], and thinking, and imagining, etc. On the other hand, there are people who can be the carpenter. [A] carpenter knows pretty well what kind of house will be. 
> 
> But even though you become an onlooker or carpenter, you never have a chance to *live* in that house. If you live in that house: well, the world of conceptualization is not perfect, blueprint is not perfect, [so] you will realize many things, [like] something wrong. Is that clear? 
>
> I'm not criticizing carpenters or blueprints. I am talking about the usual world of conceptualization, [which] you always enjoy very much, you always live [in]. Naturally, the world of conceptualization we live in is not perfect, but it is important for us, because without [the] blueprint we cannot live. Okay? But a point is, you have to see the house in terms of [a] practical point of view; in other words, in terms of the person who tastes the house through his life, every day. So there is a very close, deep communication with a house and a person. Even though you believe blueprint is perfect, if you [actually live there], there are many things you will find: a good point, a weak point, many things. Sometimes, nothing to say. 


> I think another example is the relationship between a piece of paper and fire. If you burn the paper, probably you may say paper is something separate from the fire. In terms of the world of conceptualization, it's very clear: you can see the existence of the paper separate from the fire. But actually, what do you mean by “burning the paper,” in terms of [...] flow activity, flow process between fire and paper? In other words, in terms of the true reality of the fire and paper. Can you separate [them]? You cannot separate [paper and fire], because paper is fire, fire is paper. But if I use [the words] “paper is fire, fire is paper,” it's already dualistic. 


> If you look at Katagiri, Katagiri is here and Zen Center is here. Okay? Katagiri [is working] hard at it! Aren’t [I]? But, there is nothing else to say beyond hard work or not hard work, because I am only Zen Center. I am Zen center, so I have to do it, beyond hard work or not hard work. As long as Zen Center exists in this world... well, I cannot stop living, anyway. I have to live. So I must see or hear or understand Katagiri through the true reality between Katagiri and Zen Center, which are merging, interfused completely. So, what is Katagiri? Katagiri is just flow activities. There is nothing to [put a] name on. 
> 
> At that time, within that flow activity, flow practice, sometimes you can see the result named *Katagiri*, sometimes you can put the name on it so-called *Zen Center*. That *Zen Center* or *Katagiri* is just like a flashing light. So you can see the flashing light, Katagiri. And then, I am very involved in that name of Katagiri, and then stumbling, and grumbling, always. That is [the] human problem is going. Okay? But anyway, even though I can see [lots of the] flashing lights, [the] point is I have to go back to that real reality, true reality, and constantly I have to live, and pass by that flashing light as soon as possible. 


Katagiri Roshi provides a relatively short explanation of “dropping off body and mind” in the question and answer section:

> There is no particular thing objectively you can see, or there is no particular thing seen objectively as subject (or subjective). While you can see the something subjective or objective, that is the world of conceptualization you can see. You don’t believe [it] actually, but if you really devote yourself as a practice, you do it!
> 
> If you don’t believe it, I always mention that book, *[he laughs,]* “Flow Experience,” you know? (*Transcriber’s Note:* The book is *Beyond Boredom and Anxiety*; the updated version is now titled *Flow: The Psychology of Optimal Experience*.) You know, the mountain climbers, football players... look at those people who are exactly participating in the practice, action itself. Where is dropping off the body and the mind? Your body and mind is really flexible. There is no frame of your body and the mind right in the middle of flow practice of playing football. No! If you see [it] even slightly, you will be *hurt*. You cannot play football [that way].
> 
> So you don’t see yourself particularly as a subject, you don’t see something objective, so-called ball. No, you cannot see. But there is something: ball and you communicate totally, right in the middle of flow practice of playing football.
> 
> Without this, you cannot see *any* development, any progress. If you see the progress, and then, where are you heading for? Nowhere. All you have to do is just, you have to be right in the middle of flow progress. That’s it. Every moment you have to do it. No other place. 
>
> – From [“Zazen: Dropping Off Body and Mind” at ](https://katagiritranscripts.net/1987-01-24-Zazen-Dropping-Off-Body-and-Mind)



Note that the additional characters “自然” which are translated as “of themselves” are more often translated as “naturally.” As an aside, it might be observed that Katagiri Roshi uses the words “very naturally” repeatedly in almost all of his talks. Whether there is a connection there must be left to the reader/listener to decide.


> So *sanzen* is *zazen*. How can you surrender to simplicity in life? Dōgen Zenji [says], that is zazen. 
> 
> And then he says zazen is *shinjin datsuraku*, that means “casting off body and mind,” in other words “dropping off body and mind.” Or, he says, “Dullness and distraction are struck aside from the beginning.”
> 
>  Dullness and distraction are not something you try to remove. If you try to remove [them], you create more distraction and dullness. Because dullness and distractions are something that [is] created, produced, by your attitude, by your actions, activities – so, according to [...] conditional elements, conditional circumstances. So you don’t know how to be free from [them]. No matter how long you use techniques – psychologically, philosophically, or scientifically – you never get freedom from dullness and distraction. The moment when you feel freedom from dullness and distraction, immediately you are confused right in the middle of freedom of dullness and distraction. That’s why human beings constantly seek for the psychologist to let you be free from dullness and distractions, you know? You always feed the psychologist. *[He laughs.]* 
> 
> So at the dropping off body and mind if you do zazen, simultaneously the dullness and distractions are struck aside from the beginning. This is a key point of zazen. That’s why Dōgen Zenji [says] “This is the essential art of zazen.”
> 
> Let me say [more about] this. What do [we] mean by “dropping off body and mind the moment when you do zazen, the moment when you devote yourself in zazen”? Let me say it like this. 
> 
> [...] Let’s imagine that you [are getting into] a hot bath in the cold weather. In the rigors of Minnesota winter, your body becomes very cold. After that, you put your body right in the middle of a hot bath, okay? The moment when you put your body and mind in the hot bathtub, what do you say?
>
> **Several people:** “Ah.”
> 
> **Katagiri Roshi:** “Ah!” *[Laughter.]* 
> 
> That’s pretty simple! “Ah!” – that’s it. It’s no particular word, [just] a simple word. “Simple word” means a ground word, coming from the bottom of your heart. When your body and mind becomes one with the hot water and bathtub and all circumstances – including your memories, and distractions, dullness, all stuff. And then when you become completely one with the [bath], then you can demonstrate simplicity in life – so-called, “Ah!” That’s it. 
> 
> Within the “ah” – who are they? Can you pick up something particular? Pay attention to just the moment, at the very moment when you say “Ah.” *Who* are they? What is it? What is there? Can you say it? 
> 
> *After* “ah,” you pick up *you*, who says “ah.” But I am talking about *before* you say “ah.” Okay? 
> 
> Here is a partition, a very thin partition, just like a very thin curtain.Very thin silk. Not silk... silk is still touchable, but that partition is not touchable, but it’s still something there. Just like a mist. A mist is pretty hard to grasp, but it’s there. And then if you touch it, it disappears, and you can get next door. This is a [...] door. 
> 
> So [...] you are coming back to your home, and you put your body and mind in the bathtub. And then immediately within this partition you create your own life, so-called “ah.” Simple life. And then right before this partition, right before you touch [it] – this is the very beginning of the moment, okay? The very moment, before you think of it, before something runs through your consciousness. In that [situation], I think your body and your consciousness and the water become exactly one. That situation is never described. But your body and the water [are] functioning simultaneously, together.
> 
> And then, the next moment, you say, “Ah.” That is the next moment. And then when you say “ah,” people are very interested in the “ah” which you have demonstrated. Then, you are involved so much in what “ah” means. *[Laughter.]* What are they – the hot water, and your body and mind? Who makes me say “ah”? Something like that. This is “scientific,” you know? Modern civilization. And then finally, you don’t know where you are going. And also, you completely forget the first stage, the very first stage of your life. Completely you forget. 
> 
> [In the] first stage of your life, there are many beings which are functioning interpenetratedly, interconnectedly, together. This is *oneness*. Look at this sunny, wonderful day, you know? Well, how many beings exist? When you feel that wonderful sunny day, you say, “Ah, wonderful!” And before you say “wonderful,” how many beings are working together, interpenetratedly, without any hindrances? This is called *the universe*, we say; this is called *oneness*. In the oneness, that is a place where all beings come together and are working together and walking hand in hand, without hindrances, creating a peaceful world. 
> 
> Even [beyond] Minnesota. The rigors of Minnesota winter shake hands with the winter of Hawaii, in peace. You don’t believe it, but this is true. The Japanese monkey talks peacefully with the elephant in India. Can you believe it? You don’t believe it. But this is the place where all sentient beings come together and talk together, which is called *oneness*. We say *universe*, we say the *truth*. 
> 
> But if you are involved so much in the dualistic world, *after* creating a “wow,” you completely forget that first stage of your life. That’s why spiritual life is constantly to let you [get] back to the first stage, the first stage of a “wow.” That’s it. 
> 
> That’s why you don’t understand it. But when you are there, completely the dullness and distraction, the form of the five *skandhas*, are struck aside from the beginning. And then, what do we mean? Your body and hot water becomes one. This is called *intimacy*, perfect intimacy. *Secret* intimacy we say: very secret intimacy. No gap between. 
> 
> This is called *right*, [this is] the meaning of the *right*. And also that is a gate, entrance, to communicate with the universe. *Universe* means the total picture of your life working together with all sentient beings. Okay?
> 
> So that is called *dropping off body and mind*. When you do zazen, immediately you say “Ah!” That’s it. But you don’t say “ah,” because zazen has no particular object, so-called *bathtub*, you know? So that’s why you don’t know. You are always using your mind and body, and that’s it. That is subjectivity and also object. And then the whole world comes into you. 
> 
> And then, when you say “Wow!” this is called *samadhi*, we say. *Concentration*. Total concentration, total devotion. And also this is called *jijuyu samadhi*, “self-joyousness.” *Self-joyous samadhi*, we call it. 
> 
> In other words, this is called, “Ah!” That’s it. But in zazen, you cannot say “ah,” because everyone [is] quiet. *[There are some chuckles.]* So, you have to enjoy the self-joyous samadhi concentration right in the middle of zazen.
> 
> This is “dropping off body and mind.” 


> So if you practice like this, very naturally dharma is coming to your life, and your life manifests yourself as dharma. So very naturally your life [manifests] as *total personality*. 
>
> Do you know the [term] *total personality*? Total personality is your personality *including* trees’ life, others’ life, all beings. Your life is penetrating to the past, present, future, and also trees, birds... Japan, China, all of the world... pebbles, air... and then your personality becomes *whole*. This is *total personality*. 
> 
> You can do [this]. My teacher did it. My teacher *showed me* this always. But I was young, that’s why I didn’t have enough eyes, enough ears to listen or to see it. That’s why I complained and I always was confused. But on the other hand, I felt relief when I came back to the temple, because the world is very busy, noisy, et cetera. That is [that] really, practically I can take a deep breath from his total personality. So that is wonderful. 
> 
> So total personality [is there] if you practice like this. Even though you don’t understand the meaning of *dharma* in terms of Buddhistic understanding, anyway practice like this; then your dharma comes to you and lets the flower of life force bloom. [It] is not your business [to] try to know it. People know it; people know [the] total personality coming from your heart. It’s not something you try to produce. All you can do is to practice this day to day; then naturally, total personality is [ripened]. 
> 
> So I think this is wonderful practice for us, day to day. If you study Buddhism, the concept of dharma is very complicated, so we don’t understand it exactly, but I think if [I talk about dharma] it is very helpful for you because you can practice dharma day to day. 
>
> So you should accept your life [as] totally forgiven, and you should take care of your life [as] totally forgiven, and also others’ life. On the other hand, you are never forgiven. You [will] never be. That means you should take really take best care of your life day to day. This moment never comes again. 
> 
> So how can I say it? Can I be forgiven, or not forgiven? No way. So you have to do it. That is [the] very serious and also very soft basis of human existence from which you can take deep breath. Like a wind blows; breathing blows naturally in the field. 
> 
> – From [“Depending on the Dharma” (August 3, 1988)](https://katagiritranscripts.net/1988-08-03-Depending-on-the-Dharma)

- need to come back to this one:

> And then also, if you do zazen, the original face of existence appears, manifests itself. That is, as Dōgen says in *Fukanzazengi*, [perfect and all-pervading]: the origin of the way, the origin of existence, is perfect and all-pervading. That is *buddha-nature*. If you do zazen, immediately [it] appears. That is what is called the original nature of existence manifesting itself. So Dōgen says in *Fukanzazengi*.
>
> – From [“Fukanzazengi: Dōgen's Universal Recommendation for Zazen – Talk 2” (June 10, 1979) at 34:20](https://katagiritranscripts.net/1979-06-10-Fukanzazengi-Talk-2#3420).


“Original face” is discussed in connection with *total personality* and *buddha-nature* at the beginning of [“*Fukanzazengi* – Talk 2”](https://katagiritranscripts.net/1979-06-10-Fukanzazengi-Talk-2). See also [“*Fukanzazengi* – Talk 6”](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6) after [1:16:36](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6#11636), and [“Blue Cliff Record Case 25: The Hermit of Lotus Flower Peak Holds Up His Staff, Talk 2”](https://katagiritranscripts.net/1981-11-22-Blue-Cliff-Record-Case-25-Talk-2) after [1:00:05](https://katagiritranscripts.net/1981-11-22-Blue-Cliff-Record-Case-25-Talk-2#10005). 

Just as “dropping off body and mind” is closely related to “from the first, dullness and distraction are struck aside,” “your original face will manifest” is closely tied to “the right dharma is manifesting itself.” This is implied in [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 1”](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1); where it’s discussed as “the original nature of the self is manifesting” and “manifesting the original nature of existence.”





“Body and mind dropping off” is discussed from the standpoint of Buddhist psychology in [“Fukanzazengi: Dōgen's Universal Recommendation for Zazen – Talk 6”](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6).

Another clear reference is in [“Principles of Practice, Talk 4: Faith”](https://katagiritranscripts.net/1986-03-22-Principles-of-Practice-Talk-4): “So that is, if you put your body *right there*, then you can drop off your body and mind, drop off, you can be free from the root of discriminating mind. That means you can be exactly one with the very minute vibration of the mind. And then, no concept of the minute vibration of the mind.”

“Dropping off body and mind” is closely related to “from the first, dullness and distraction are struck aside.” This is mentioned in [“Zazen: Entry to the Buddha Dharma”](https://katagiritranscripts.net/1987-03-07-Zazen-Entry-to-the-Buddha-Dharma). See also the notes for “dullness and distraction are struck aside” below, closer to the end.

A good search term in KR’s talks is “drop off.” There are many references to things that “drop off”: delusions, dullness and distraction, verbal explanations, all unwholesome things, all unwholesome human behaviors, thought and discursive thinking, ideas, the “concept of wondrous practice which you have realized” ... and so on.

```{=typst}
#pagebreak()
```

# Chapter 11: Practice Suchness Immediately

## Paragraph 4 Part 4

> 欲得恁麼事、 急務恁麼事。  

> If you want to realize such, get to work on such right now. [SZ] 

> If you want to attain suchness, you should practice suchness without delay. [EB]

## Commentary

> And then next, Dōgen Zenji [says], 
> 
> > Everyone is endowed with body and mind, though their actions inevitably vary, being either strong or weak, brave or cowardly. It is through the daily actions of our body and mind, however, that we directly become Buddha with our body and mind. This is known as realization of the Way.
> 
> Here it says “realization of the Way”: *jōtō*. So, *jōtō*, to assimilate and actualize *it*, is to become Buddha with your body and mind directly. Not to become Buddha *after* doing something. Okay? 
> 
> We always think, “By practice, *then* I will be Buddha. I am not good, that’s why I want to practice. and then after practice, I will be Buddha. I will be a good boy.” This is dualistic. So *jōtō* is directly you have to become Buddha with whole body and mind, your body and mind. This is *jōtō*. 
> 
> Well, without *jōtō*, assimilating and actualizing *it*, no one grows, no one is educated. That is real education of human beings. Because everyone lives in that way. 
> 
> But people misuse that *it*. Okay? Even though they are there. They are present in it, but they always misunderstand and misuse. So very naturally, if you don’t teach that way, teach *jōtō*, assimilating and actualizing *itself*, *it* – you cannot educate anybody properly. 
> 
> Of course, school educates many people. But what does school teach? I don’t think school teaches how to assimilate *it*, how to realize *it*. No. [It’s] always *something* floating on the surface of oceans – always we teach those. We completely forget *it*, where we always are present in it. 
> 
> So we have to teach this. That’s why Zen Buddhism teaches that. Otherwise you cannot grow, you cannot educate yourself, you cannot teach, you cannot help anybody.
>
> 34:07 1986-03-23-Principles-of-Practice-Talk-5



“Such” or “suchness” here is *renme* (恁麼) in Chinese or *inmo* (いんも) in Japanese. Note that there is a whole chapter of *Shōbōgenzō* on the subject of *inmo*, appropriately titled *Inmo*. Essentially *renme* or *inmo* is an informal expression of *nyoze* (如是).  (Source: *Treasury of the True Dharma Eye: Dōgen’s Shōbōgenzō, Volume I-VII*, by the Sōtō Zen Text Project, “*Inmo*.”)

“Realize” or “attain” here is a different character from *shō* as “realization” that we discussed earlier, but Katagiri Roshi treats it as the equivalent in his discussion of *nyoze*:

> In *nyoze*, *nyo* is “like” or “thus” – “look like.” But in Zen Buddhism, *nyo* means “look like” but on the other hand *nyo* is direct manifestation of something ultimate. That is called *nyo*. 
> 
> So Dōgen Zenji says in *Genjōkōan* (actually in *Zazenshin*) “birds fly like a bird, fish swim like fish.” That means exactly fish become one with the water, and birds’ activities are completely identical with the function of the air and sky, all sentient beings. At that time, we can say birds are not birds, birds are sky. So that is called, Dōgen Zenji says, “Birds fly like a bird.” Because it’s pretty hard to say it is *bird*, because it is sky, it is air – without this situation, a bird cannot fly in the sky. So *bird can fly* means to be supported by air and sky and clouds and all sentient beings, and then the life of birds is supported. That is called *to be able to fly*, for a bird. So that we can live is [because our life is supported] by many beings. At that time, Katagiri lives like Katagiri. Not *exactly* Katagiri – at that time, Katagiri becomes exactly *jijuyu samadhi*. [Or] *buddha*. 
> 
> So that is, [Dōgen Zenji] said, *nyo*. The Chinese character is called *nyo*, of *nyo ze*. *Nyo* is “thus” or “look like,” but it means pointing out exactly *consummation of being*. That is *nyo*. 
> 
> Because it’s pretty hard to say: if you’re really alive in this world, creating peace and harmony, you are you, you look like you, but you are not you, you are something more than you. You yourself don't know how you can get [this] energy. From the small five *skandhas*? No. You don't know [how], if you really live in peace and harmony with all sentient beings. Very naturally you can feel this. So [...] it’s pretty hard to explain who you are, where you can get such a kind of energy, et cetera. So we call it *nyo*. 
> 
> *Ze* is “this.” That *nyo*, “thusness,” is something existent right now, right here. That is called *this*. So *nyoze* is translated as *thusness*, or *suchness* sometimes. So *nyoze* is what is, just *is*, of itself. 
> 
> So that is the place where all living beings coexist in peace, and ... synchronize with each other in peace and harmony. That is *shō*, “realization.” 
>
> – From 1987-03-15-Bendowa-Talk-5

It’s also worth noting that *nyoze* is translating the Sanskrit word *tathātā* (“suchness”, “thusness”),  which is related to the word *tathāgata*: “one who is thus coming and going” – another title of a buddha.

*Jíwù* 急務 means something like “urgent task” or “pressing matter.” “Get to work” might be a logical translation of *Jíwù shì* (急務事), but in this context it carries some unnecessary heaviness. “Get to work” also tends to imply a goal, which might not be the case here.

So a better translation might be: 

> If you want to attain *suchness*, practice suchness immediately.

This is pretty close to the Eastern Buddhist translation, except “immediately” may be a better word than “without delay,” as it’s more a matter of directness than of avoiding procrastination.

This is also close to the translation used by Confluence Zen Center ([external link](https://www.confluencezen.org/fukanzazengi/)), and that used by Zenkatsu Norman Fischer ([external link](https://everydayzen.org/teachings/fukanzazengi-2/)). 

```{=typst}
#pagebreak()
```

# Chapter 12: Surrender to Tranquility

## Paragraph 5 Part 1

> 夫參禪者、 

> For practicing Zen, ... [SZ]

> For the practice of Zen, ... [EB]

## Commentary

In Chapters 1 through 8, we discussed *why* we should do zazen, and in Chapters 9 through 11 we discussed *what* that means. In reality, of course, there is considerable overlap in these areas; we’ve really been discussing *what* zazen is and *why* to do it all along, and will keep doing so. Nevertheless, we could say in a broad sense that in Chapters 12 through 25, we now turn to *how* to do zazen. This is the part that includes details of the form of sitting Zen meditation. 

But before we step into the details, we actually need to back up and look at the big picture once again, because right away we encounter an important term: *sanzen* (參禪, or 参禅 in simplified Chinese), which is often translated as “Zen practice.” So the opening of this section is usually translated as something like, “For the practice of Zen.” But *sanzen* means something deeper than we may hear from the English words “Zen practice.”

---

Katagiri Roshi explains why he prefers to leave the term *sanzen* untranslated:

> *Sanzen* means literally to surrender yourself to tranquility or simplicity in life. To surrender yourself or to submit to perfect tranquility or simplicity in life; this is called *sanzen*. Usually *sanzen* is translated as “practice,” but “practice” in English doesn't hit the mark to *sanzen*.
> 
> *Fukanzazengi* [which we] chant every evening uses the original term *sanzen*. So remember, *sanzen* is to surrender yourself to tranquility or simplicity in life. 
>
> – From [“Zazen: Dropping Off Body and Mind”](https://katagiritranscripts.net/1987-01-24-Zazen-Dropping-Off-Body-and-Mind).

According to the Internet, *san* (參) means “to participate” or “to visit.” In fact, some Zen centers use the word *sanzen* to mean “meeting with a teacher.” That is not the sense of the word in *Fukanzazengi*. In response to a question, Katagiri Roshi explains why he uses “surrender”:

> The *san* of *sanzen* is “to surrender” or “submit” ... or “to visit,” actually. To visit. Okay? *[They laugh.]* You cannot visit [Zen or tranquility] objectively; if you want to visit, your body and mind must be there. That is called *surrender*. You have to surrender yourself to, otherwise you cannot visit.
> 
> So, that is the *san*. *Zen*, linguistically, that is “to manifest simplicity.” So that’s why “to submit yourself to the simplicity or tranquility,” that is *sanzen*. 
>
> – From  [“Zazen: Dropping Off Body and Mind” (January 24, 1987) at 51:02](https://katagiritranscripts.net/1987-01-24-Zazen-Dropping-Off-Body-and-Mind#5102).

In his series of talks on *Gakudō-yōjinshū*, [“Points To Watch in Buddhist Practice”](https://katagiritranscripts.net/principles-of-practice), Katagiri Roshi says that this surrender to tranquility is the study of the Way, and is the purpose of spiritual life:

> The purpose of spiritual life is to actualize *sanzen gakudō*, which means to surrender one’s body and mind to tranquility. *Tranquility* means the Way: to surrender one’s body and mind to tranquility is to study or to learn the Way. 
>
> – From [“Principles of Practice, Talk 2: Bodhicitta” (March 20, 1986)](https://katagiritranscripts.net/1986-03-20-Principles-of-Practice-Talk-2).

We discussed in Chapter 1 the meaning of *Dō* or *Dao*, “the Way,” but it’s important to review it here so that we can understand *gakudō*, “studying the Way”:

> *Gakudō* means “to learn or to study the Way.” *Gaku* means to learn or to study. *Dō* is the Way. So *gakudō* is a pretty technical term Dōgen Zenji uses very often: *gakudō*, to study or to learn the Way. 
>
> *The Way* means the universal life beyond conscious or unconscious worlds. This is the Way, where all beings exist in peace, in harmony, prior to the germination of any subtle ideas. [...] All sentient beings exist in the realm of the Way; that is called *universal life*. This life is open not only to human beings or living beings, but also inanimate beings: pebbles, water, et cetera. 
>
> So *gakudō* is to study the universal life beyond the conscious and unconscious worlds. This is *gakudō*. 
>
> – From [“Principles of Practice, Talk 1: The Purpose of Practice” (March 19, 1986)](https://katagiritranscripts.net/1986-03-19-Principles-of-Practice-Talk-1).

Katagiri Roshi explains why *zen* in this case means “tranquility”:

> *Sanzen* is to surrender one’s body and mind to *zen*, or tranquility. *Zen* sometimes means *samadhi*, one-pointedness; sometimes it is translated as *tranquility*; sometimes it is translated as *meditation*. But anyway, *san* means “to surrender oneself to.” To surrender, or to visit, to be present... to go toward. This is *san*. So *san-zen* means to surrender one’s life to *zen* or tranquility. 
> 
> *Zen* or tranquility means [the] dimension of being in which there is no individual consciousness, so-called consciousness or unconsciousness. So [no] subtle signs of ideas, conscious world or unconscious world. 

But when we hear the word “tranquility,” what does that mean to us? What does “tranquility” feel like? 

---

Katagiri Roshi clarifies what this kind of tranquility means: 
 
> In Japanese, tranquility is called *jakujō* (寂靜). *Jaku* means perfect stillness – perfect stillness just like [there is] no one or nothing with which you want to talk, you want to see. So, perfect tranquility. That means if you are there, you are *exactly* there; nothing else except *you*. So that is very tranquil. Just like being present in the wilderness: there are lots of beings there – insects, birds, trees, skies – but if you are in the wilderness you feel perfect tranquility. That is the meaning of *jaku*. So, completely nothing around you. 
> 
> And also *jō* of *jakujō* means literally “to express in detail.” So literally [...] *jō* of *jakujō* is also the same meaning of stillness or tranquility, but it is a little different from the *jaku* of *jakujō*. *Jō* is “[tranquility and stillness] which penetrates every aspect of everydayness.” 
> 
> So *jaku* is kind of the essence of beings, how they exist. Everything exists exactly in peace, in harmony, in tranquility. But it is not something *abstract*, because it penetrates every aspect of everydayness. If you see a tree, if you see winter, if you see fine days – whatever you see, all sentient beings exist just exactly tranquil. You can see perfect tranquility through the form [of beings], every form of beings – trees, birds, and the weather, et cetera. So that’s why *jō* of *jakujō* is tranquility which penetrates every aspect of everydayness. 
> 
> So *jaku* is no one or nothing with which you want to talk; that is, according to [what Buddha said] or according to [Buddhist] teaching, we say, “Heaven and earth is the same and one root as my existence, your existence.” [Or] “I and heaven and earth are the same and one root.” That is called tranquility, exactly tranquility. Tranquility is no ideas, nothing to think. So you cannot think of it. Before you think of the universe, or you – whatever – the whole world, all existence exactly exists in perfect peace and harmony. That is called “I and heaven and earth are the one and the same root.” 
> 
> The *jō* of *jakujō* [is], according to Buddha’s teaching, we say *hachimen reirō* (八面玲瓏). That means a clear and immaculate jewel with octagonal spheres. “Octagonal” [here] doesn’t mean eight angles or eight dimensions of the jewel or ball, [it means] many angles there. 
> 
> So existence is just like a huge ball or jewel which is clear and immaculate. That is *jaku*, exactly: perfect quiet. But on the other hand that ball has many aspects, many angles: that is called “octagonal spheres.” (That is *jō*.) That means many myriad, myriad aspects of human life, every day. Getting up in the morning; washing your face; having your breakfast; studying; working. Many aspects appear in one sphere, in one situation – one and the same situation which is called *perfect*, clear, and immaculate.
> 
> This is the meaning of *sanzen*. So it’s very difficult to translate *sanzen* into English. If you say “the study of the Way through the practice of zazen,” it is true... but it is pretty difficult to express the real spirit of the practice. So I want to use this original term *sanzen*, so through this original term you can see the real spirit of practice.
>
> – From [“Principles of Practice, Talk 1: The Purpose of Practice” (March 19, 1986)](https://katagiritranscripts.net/1986-03-19-Principles-of-Practice-Talk-1).

Putting it all together:

> So let’s [look at] the meaning of *sanzen gakudō*, okay? *Sanzen* is you have to surrender your whole life to *zen* or *tranquility*, which is exactly the Way. So *sanzen* is the same meaning as *gakudō*. What do we learn? The Way; it is the Way. 
> 
> But what is the Way? That is universal life. What is universal life? How do we learn that universal life beyond [the] conscious and unconscious world? 
> 
> You have to surrender your whole life to tranquility. Tranquility means perfect tranquility, stillness, [and] on the other hand that perfect tranquility penetrates every aspect of everydayness. So to surrender yourself to tranquility *totally* means you have to manifest perfect tranquility within each single form of everydayness: *gassho*, getting up in the morning, having breakfast, walking, et cetera. 
> 
> That is the meaning of *sanzen gakudō*. 
> 
> – From [“Principles of Practice, Talk 1: The Purpose of Practice” (March 19, 1986)](https://katagiritranscripts.net/1986-03-19-Principles-of-Practice-Talk-1).

The first line of Dōgen Zenji’s *Zazengi* (which is different from *Fukan Zazengi*) says:

> *Sanzen* is *zazen*.

This was one of the main teachings of Dōgen’s teacher, Tiantong Rujing: “Sanzen is zazen.” Katagiri Roshi explains why this is so:

> Simplicity is manifested only when your circumstances are very simple and neat, clear. That's it. At that time, that is great opportunity or great chance for us to manifest simplicity in life or tranquility in life. 
> 
> It's very difficult to manifest simplicity, tranquility in a complicated world. But we live usually in a complicated world; that's why [we ask] how can we manifest, how can we find [...] simplicity in the complicated world. This is a little difficult point for us. But we have to do it. That's why every day we try to practice.
> 
> You don't realize [the] great capability you have, enough to become an artist, but originally you have [it]. But we don't know. That's why within the world we don't know, we have to build up the world we have already possessed. So that's why [it’s] a little difficult for us. 
> 
> That's why *sanzen* is *zazen*. In order to submit to tranquility or simplicity in life, [that] is to do zazen. [...] 
> 
> – From [“Zazen: Dropping Off Body and Mind”](https://katagiritranscripts.net/1987-01-24-Zazen-Dropping-Off-Body-and-Mind).

Arranging circumstances so as to manifest simplicity is the topic of the following chapters, where we examine the form of zazen in detail.




```{=typst}
#pagebreak()
```

# Chapter 13: A Quiet Room is Suitable

## Paragraph 5 Part 2

> 靜室宜焉、飮食節矣。

> ... a quiet room is suitable. Eat and drink moderately. [SZ]

> ... a quiet room is suitable. Eat and drink moderately. [EB]

## Commentary

Making arrangement: revist:
> So, very naturally, the important point is [that] practice must be total manifestation of ultimate nature of existence, and ultimate nature of existence is simultaneously present with your practice. Because ultimate nature of existence is not your business. It is not something *you* try to manifest. No. You have to arrange circumstances, [arrange] your body and mind to be in peace and harmony, and then, ultimate nature of existence comes out naturally. Like the moon comes out from the clouds. Like this. 
>
> – From [“*Bendōwa*: Dōgen's Questions & Answers – Talk 5” (March 15, 1987)](https://katagiritranscripts.net/1987-03-15-Bendowa-Talk-5)



On several occassions, Katagiri Roshi say that there are three main areas to pay attention to in zazen: body, breath, and mind:

> ... there are three crucial points you have to pay attention to in zazen: harmonizing the body, harmonizing the breath, harmonizing the mind. That is very important.

This list of three things comes up often. And in addition to this, there is your external environment to consider:

> In this case, first of all you have to make arrangement of circumstances: the zendo, sitting place. So, not a messy room, not a stinky room; not too bright, not too dark; not too cold, not too hot; not much [draft]. You should adjust the external circumstances for your sitting. 

In his 1979 series of talks on *Fukanzazengi*, Katagiri Roshi covers this in a slightly different way. He says that there are several component factors of our life, psychologically speaking:

1. Circumstances; the environment.
2. The sensory system.
3. The movement system. 
4. The internal organs
5. The brain / nervous system.
6. Total personality.

We introduced total personality as an important concept in Chapter 1, but here Katagiri Roshi talks about it in more detail. He explains that total personality is the core of our living, but in order to realize it we have to “make arrangement” of the other factors, on whichever list we are going by. He says:

> *Total personality* is exactly the center of your living, the core of your living. Without total personality, you cannot get circumstances, or sensory world, or movement system – nothing there. 
> 
> There is Katagiri: that core of Katagiri is really supported by total personality. Total personality is the character created by Katagiri in the past, in the present, in the future. My parents, my grandparents, and my ancestors; that is *total* personality. 
> 
> *My* personality is something *I* can create after my birth. But this is kind of *character*. If you say *personality*, psychologically speaking, this is a little bit broad. So *my* personality is something I can create after my birth, but there is another personality I [can’t] create, [where] I have carried my personality from before my birth. This is maybe my parents, and also maybe I have carried [it] from [...] my grandparents, from my grand-grandparents, and ancestors. That is *total personality*, the *whole* personality. 
>
> So if I see myself – here is Katagiri – immediately there is a certain kind of a “smell.” [...] A part of this *smell* consists of something I have created after my birth, but the other aspect of my *smell* is something I have carried before my birth: from my parents, grandparents, grand-grandparents, and ancestors – maybe from before the world began. So at that time, that personality is really a smell. If you see somebody, there is a smell. Katagiri smells. 
>
> But Katagiri’s *smell* is a kind of a result that we have judged. From where does that smell come? If you research again and again, finally there is no evaluation, because you don't know from where it comes. You have to go back to the beginningless past; you have to go back. And you have to go to the endless future. And *then* you can understand. 
> 
> So finally, that smell is something not evaluated. That is called *buddha* – or, the *original nature of existence*. But psychologically speaking, that is called *total personality*. Total personality, or maybe *trans-personality*, whatever you say.
> 
> But immediately [you smell this trans-personality]: “*I* smell something; I smell myself as Katagiri.” So at that time it's pretty hard to adjust, to make myself in peace and harmony, in an evil sense. But in a good sense, I feel good – [but] feeling good is not always *feeling good*, *[he chuckles,]* not always helping you. Sometimes it becomes a “stink.” 
> 
> So whatever *I* feel from my personality, [...] there is always some confusion, waves of the mind. Feeling good, feeling bad; whatever you say, that is a wave. Because that feeling comes from “stink,” which is called total personality. 
> 
> Because I don't know what my karma is. Why did I become a monk? I don't know. I know *why* – but on the other hand, there are lots of reasons. I don't know why [exactly], so I cannot say. 
> 
> That is really a stink. [...] But that stink is completely [beyond evaluation]. From where does that stink of Katagiri come? No way. You have to really go back to the beginningless past, to the endless future.
> 
> So finally, that stink of Katagiri, which is called *total personality*, becomes *trans-personality*. That is the original nature of existence. That is the core of your daily living. You are already under this core, under this huge tree. It's vast, a *huge* tree. Because [your existence] is extending to the past and the future; your personality.
> 
> You have to believe this. Well – believe it or not, your life is really there.
> 
> So that is [that] we are called *buddha-nature*. And also, what is buddha-nature? If you want to know psychologically, that is called *alayavijñāna* in Buddhist psychology. Or sometimes, primitive Buddhism says that is *karma*. 
> 
> Karma is completely beyond good or bad, right and wrong, but simultaneously karma is something which is very powerful to carry your life in the samsaric world. Anyway, if you want to know karma, you have to go back to the beginningless past, and to the endless future. Finally, there is no answer [to what karma is], but karma is with you. How do we know? In your daily living, you can know. 
> 
> When I became a monk and went to a monastery, at that time monastic life was completely blooming for me. It really awakened me, every day. My eyes [were] opened wide, and [I was] looking at everything, and I learned lots of things. Some other monks were always creating a dull feeling, and indulgence, and they didn't like sometimes doing zazen, and laziness... [*He chuckles.*] But for me, it was wonderful. 
> 
> And on the other hand, I felt wonderful, but people called me crazy. Of course, maybe so! According to indulgence, maybe to practice hard was crazy, it makes you crazy. But I didn't care, because I learned lots of things. Day after day was really bright. So I just did it.
> 
> On the other hand, there is a completely opposite aspect of life I learned from other monks. I really wanted to ask them, “Why do you do it in that way? Why are you in the monastery? You want to be lazy in the monastery? You want to learn laziness? Well of course it's okay, but what is the purpose? *Why*? Why are you here?” I didn't understand why they didn’t care.
> 
> [And] on the other hand, the same applied to me: “Why are you practicing hard in that way?” I don't know.
> 
> From this point, we can create our own everyday life, but on the other hand there is another aspect of life we cannot create, [which] something compels us to do. So, our daily living is in some aspect understandable, but our daily living is in some sense *not* understandable. Life is pretty [big]. 
> 
> That is called *karma*; that is called *buddha-nature*. We don't understand, because the present – your life – comes from beginningless past, endless future. 
> 
> [We should be there]. And finally, we should accept this and we must be *present* there, constantly on the big tree. This is [the] core. Psychologically speaking, this is *total personality*.
>
> [...] In order to *realize* this core of human life, first of all we have to *make arrangement* of circumstances, and the sensory world, and also the movement system, and the gut system, and brain-nerve system. Anyway, we have to *make arrangement*. 

In these lines of *Fukanzazegi*, “a quiet room is suitable” is discussed as “arrangement of the sensory system”: 

> We have a sensory system; it's not necessary to destroy [it or] to keep away the sensory world, because we have it already. So instead of [maligning] or throwing away or destroying the sensory system, first of all we should accept the sensory system. And the important point is, how to use the sensory system. 
> 
> That's why Dōgen Zenji says,
> 
> > A quiet room is suitable.
> 
> Or,
> 
> > Do not allow drafts of air to enter, or rain and frost to intrude.
> 
> Or, 
> 
> > The place of sitting should be lighted, and kept from becoming dark at any time, day or night.
> 
> > Eyes should be open, not too widely, nor too narrowly.
> 
> (*Transcriber’s Note:* “Do not allow drafts of air to enter” etc. is from the *Zazengi* chapter of *Shōbōgenzō*, which is distinct from *Fukan zazengi*.)
> 
> This is how to make arrangement of the sensory world. First of all, you should make a choice of circumstances: what kind of a room you have to use. Because you have six senses. You can see this room through your eyes. It’s really dark. If you painted this wall red, green, and yellow, [you would see it] completely differently, don't you think so? And also if this room is too dark, it's not good; if this room is too bright, it distracts your mind, distracts the sense of vision. And also, if you choose a room in a very noisy location, it really distracts the sense of hearing. So the important point is, “A quiet room is suitable,” and also, “Not too dark, not too bright, at any time, day or night.”
> 
> So that is how to make arrangement of the sensory world. Instead of destroying, escaping from, or expressing hatred toward the sensory world, we should [deal with it].

“Eat and drink moderately” is discussed as “arrangement of the internal organ system” or “gut system,” but without much detail. Perhaps this one is self-explanatory. 

> In this case, first of all you have to make arrangement of circumstances: the zendo, sitting place. So, not a messy room, not a stinky room; not too bright, not too dark; not too cold, not too hot; not much [draft]. You should adjust the external circumstances for your sitting. 


```{=typst}
#pagebreak()
```

# Chapter 14: Put Aside All Involvements

## Paragraph 5 Part 3

> 放捨諸縁、休息萬事。  

> Put aside all involvements and suspend all affairs. [SZ] 

> Cast aside all involvements and cease all affairs. [EB] 

## Commentary

This is discussed as “arrangement of circumstances”:

> That's why Dōgen Zenji said in *Fukanzazengi*:
> 
> > Cast aside all involvements; cease all affairs.
> 
> This is arrangement of *circumstances*. 
> 
> If you meddle with *all involvements* or *all affairs* right in the middle of zazen, you cannot experience calmness. You cannot stand up straight, you cannot sit quietly right in the middle of zazen, because there are too many things you are involved in. 
> 
> So first of all, we have to *make arrangement of circumstances*. Instead of expressing hatred with circumstances, or destroying circumstances, just make arrangement. 
> 
> – From [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 1” (34:20)](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1#3420).

Katagiri Roshi says that this relates to *samadhi* and *egolessness*:

> *Egolessness*: that is to regulate the mind. How to regulate the mind? Well, egolessness. How to practice egolessness? Throw yourself away. In other words, offer yourself into zazen. How can you do that? By the help of *samadhi*, one-pointedness. With wholeheartedness, you can do it – very naturally. 
> 
> So if you really want to accomplish one thing which you want to do, you have to cut off “all involvements and all affairs.” In other words, make arrangement. 
> 
> The young kids are listening to the radio and also studying and also trying to accomplish one thing – it seems to be good, but it's not the real accomplishment of doing one thing that you want to do. So if you really want to accomplish one thing with your wholeheartedness, it is very natural that you make arrangement of circumstances. This is a very natural attitude [toward] life. That's why Dōgen Zenji says, “Cease all involvement. Throw away all affairs.” Don't worry about a certain sound of the cars; anyway, throw away. 
> 
> How can you throw away? *Simplify*. You should simplify your activity, [simplify the relationship between] yourself and object. See the relationship simplified between you and zazen, or study, or playing guitar, or whatever. [...] How can you simplify? Let's practice *samadhi*. *Samadhi* is one-pointedness. If you practice one-pointedness, there is *egolessness*. Let egolessness simplify your life. [Manifest simplicity,] simplify your life. Because [then] you can offer yourself into the object: zazen, or study, et cetera. 
> 
> And then, completely simplified, unified, that is what is called *harmonious*. Or *regulating*; we use the term regulating. *Regulating* is not to destroy, not to move from one to another. Regulating means [that you know] many things around us. First, accept [them], and [then], how to *arrange* them; how to use the circumstances, the sensory system, movement system, and guts, and also the brain-nerve system, whatever it is. And then, let's sit down in the core of your total personality. That is buddha-nature. And then this total personality, which is called buddha, is completely perfect and all-pervading. Dōgen Zenji says, “The origin of the way is perfect and all-pervading.” 
> 
> And also, “manifesting the original nature of existence.” If you arrange the circumstances, and sensory world, movement system, gut system, and also the brain and nervous system, very naturally you can practice *samadhi*, you can offer yourself into [zazen], and you can practice egolessness. And also, you can do something without any design on expecting a reward. That is perfect, harmonious life. That is peaceful life.


Temporarily setting aside involvements is practically very important for zazen, but there is also a deeper meaning of “cease all affairs, all involvements” which Katagiri Roshi talks about:

> > Cease and desist; then an iron tree blooms with flowers. 
> 
> I very often emphasize that “cease and desist” is not your business. [If] you try to cease, you try to desist, [then] you never cease, you never desist. Because the more you try to cease, the more you realize that there is always something moving. So you never stop anything.
> 
> So an import point is, [it is] only when there is absolutely nothing that is your business. All you have to do is, when you sit down, you just be one with the sitting. At that time that is called “to cease all affairs, all involvements.” That is in *Fukanzazengi*. 
> 
> If you read *Fukanzazengi* carefully, Dōgen Zenji mentions making arrangement of circumstances: the room, and your body, clothes, your mind. Mainly the three adjustments: breathing, mind, and body; and also we have to take care of the circumstances. 
> 
> Arranging circumstances is very complicated. You can make arrangement of circumstances, but right in the middle of zazen, still there are complicated circumstances always occurring from moment to moment. Visualizations inside of your head; this is one kind of circumstance. If you are completely tossed away by them, you cannot cease involvements. If you are involved in this visualization inside, you never cease, you never desist. The point is that “constantly making arrangement” means you have to put it aside, and all you have to do is just have one-pointedness on zazen, breathing. That’s all you have to do. And then very naturally, that is called *cease all involvements*. And then at that time it is called *all worldly affairs rest peacefully*. The noise of cars, birds, and winter, are completely resting in this realm. That is called *cease and desist*. 
> 
> So if you try to cease, you never cease; only [when] there is nothing for your business. If you try to, or you try not to, whatever you do, it’s your business. At that time it’s very difficult to cease. So if you realize there is completely nothing for your business, at that time you can really cease. That is called *shikantaza*. I think you should really experience this through shikantaza. Otherwise, no matter how long I [explain it], it doesn't make sense. 
> 
> So, “cease and desist; then an iron tree blooms with flowers.” You don’t believe just sitting like this, without having your own business. And then you say, “And then what? Is it useful?” Or, “Is it not useful?” You always try to create your business. But just sitting is kind of nothing, no business. But [it’s] a business! The iron tree really blooms. 
> 
> I mention that Zen practice is [to] completely cut down your egoistic constructed way of life. Most people are really afraid of doing that, because people are afraid of losing the self, but I don’t think that is the right understanding. It’s pretty hard, but if you cannot do it, [then] in your everyday life there is always egoistic sense. Even [in] zazen, you have to do *real* zazen, throwing away your egoistic constructed way of life. At that time intellectually you are afraid of losing yourself, but actually [you don’t], the real self is blooming. The real self blooms from completely nothing. 
> 
> That’s why here it says, *then* an iron tree blooms with flowers. *Nothing* means just like an iron tree. It’s impossible to bloom flowers from nothing, but it really blooms from there. 
>
> – From [“*Blue Cliff Record* Case 40: Nan Ch’uan’s It’s Like a Dream, Talk 1”](https://katagiritranscripts.net/1983-01-26-Blue-Cliff-Record-Case-40-Talk-1)

In a talk on the Buddhist arts, Katagiri Roshi discusses the tea ceremony: 

> The practice of zazen is to make you forget all worldly affairs. That’s why in *Fukanzazengi*, Dōgen Zenji [says], “Throw away all affairs.” Even good and bad, right and wrong – anyway, sit down. This is the total picture of zazen; just like a tea ceremony. 
> 
> So the tea ceremony is... what would you say... the artistic expression of religion. *Not* the religious expression of art. Do you understand that difference?
> 
> So the purpose of zazen is to make you completely forget all worldly affairs, and simultaneously there must be a very compassionate consideration, [in] which there must be readiness on [your part] to be immersed in the heart of zazen. If you just be there, it’s not good enough, because still you cannot be immersed in the real heart of zazen or the tea ceremony. 
> 
> For instance, nature. If you go to the wilderness, if you are just right in the middle of the wilderness, you completely forget [...] worldly affairs. Completely beyond [whether] you try to forget or you don’t try to forget. So what is real nature? What is the heart of nature? The heart of nature is [for you to completely forget] worldly affairs. 
> 
> But forget doesn’t mean *ignore*. To forget worldly affairs means you can see the worldly affairs from a completely different angle; this is called *to forget*. Not [to] destroy, not to keep away from worldly affairs. Because your body and mind are already nothing but the worldly affairs. So what does it mean [to forget] worldly affairs? If you see worldly affairs in terms of worldly affairs, you never have a chance to see the depth of the worldly affairs, how sublime it is. So you have to see worldly affairs from a completely different angle. That is something beyond your attempt of satisfying your desires. That is the total picture of nature. 
> 
> So, just be there. Go. Sit down there. 
> 
> That’s nature, wilderness. Just like zazen. 
> 
> But is that enough for us, *just be there*? No. Still there must be compassionate consideration, that [...] you must be ready to be immersed in the heart of nature. Because, if you just be there, very naturally your desire appears and disappears, appears and disappears, so very naturally, you mishandle nature. Because you are already worldly affairs, so worldly affairs always demonstrates yourself as good or bad, right and wrong, failure or success, et cetera. So if you don’t feel good, you can destroy the nature. So nature is always used by your desires. This is human beings. 
> 
> So very naturally, you cannot hurt the heart of nature if you are there. As much as possible, you must bring the harmony to your life, and to the rhythm of nature. For this, you should accept the rhythm of nature, which it possesses in itself. 
> 
> And also you must always try to tune into the rhythm of *real* nature, what the real nature is. You have to tune in. That is human effort. 
> 
> That is called *bendo*, okay? *Bendo*; we say *practice*. *Bendo* means [to] expend your every possible effort or energy toward the way, not for the purpose of satisfying your desires. Toward the Way. *The Way* means perfect harmonious rhythm of nature, wilderness. So you cannot hurt [it].
>
> – From [“Arts and Buddhism” (October 29, 1983)](https://katagiritranscripts.net/1983-10-29-Arts-and-Buddhism)

“Throw away all worldly affairs,” et cetera is discussed in [“*The Awakening of Faith* – Talk 38”](https://katagiritranscripts.net/1986-05-02-Awakening-of-Faith-Talk-38)

```{=typst}
#pagebreak()
```

# Chapter 15: Have No Designs on Becoming a Buddha

## Paragraph 5 Part 4

> 不思善惡、莫管是非。停心意識之運轉、止念想觀之測量。莫圖作佛、豈拘坐臥乎。  

> Do not think "good" or "bad." Do not judge true or false. Give up the operations of mind, intellect, and consciousness; stop measuring with thoughts, ideas, and views. Have no designs on becoming a buddha. How could that be limited to sitting or lying down? [SZ] 

> Do not think good or bad. Do not administer pros and cons. Cease all the movements of the conscious mind, the gauging of all thoughts and views. Have no designs on becoming a buddha. [*Sanzen*] has nothing whatever to do with sitting or lying down. [EB]

## Commentary

Katagiri Roshi discusses this as “arrangement of the brain / nervous system”:

> Next, the *brain-nerve system*. About the brain-nerve system, Dōgen Zenji says, 
> 
> > Do not think good or bad; do not administer pros and cons.
> 
> Or,
> 
> > Cease all the movements of the conscious mind, the gauging of all thoughts and views. Have no design on becoming a buddha.
> 
> That is the brain-nerve system. According to the brain-nerve system, we have to regulate mind. Mind is characterized by attachment: attaching to one of two extreme ideas; this is the characteristic of mind. So, we have to make arrangement of the functioning of the mind ...
> 
> *[Tape change.]*
>
> ... “[Cease all the movements of the conscious mind, the gauging] of all thoughts and views. Have no design on becoming a buddha.” Completely throw away any germination of wishes, thoughts, and views. Just [you yourself sit] with zazen. That's all you have to do. 
> 
> Dōgen says “do not think good or bad, right and wrong” because we have to regulate [the] mind, which is characterized by attachment to one of two extreme ideas. That is mind. That's why we shouldn't attach to good or bad, right or wrong, or neutral. 
> 
> That means the practice of *egolessness*; selflessness. 
> 
> If your mind really attaches to good or bad or neutral, immediately here are thoughts, views, wishes. And thoughts, views, wishes create the dualistic world. Some go this way, some go that way; always going back and forth. And sometimes, [stopping]. [But] even though you can stop for a while, you cannot stop always, so you start to move to the right, to the left again. That is the dualistic world. 
> 
> – From [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 1” (44:56)](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1#4456).

> So you, and the universe, earth, all beings, and all circumstances, [...] become sitting with you, together. This is called *zazen*. All we have to do is to do our best to sit in the universe with all sentient beings. That’s *all* we have to do. 
> 
> Don’t expect anything *special*, [other than] this. Just do your best to do *this* zazen. Just like a spinning top. The top is spinning; just spinning. At that time, the top becomes still on the floor, very naturally. 
> 
> So that’s *all* you have to do. But if you expect even slightly something *from* zazen, zazen becomes a means to an end. At that time, [there is] *zazen* and also *purpose*. So very naturally, there is something else! So very naturally you cannot [be] always exactly sitting, you cannot do your best to do sitting, because you expect something extra, [other than] zazen. 
> 
> So when you want to do zazen, anyway, do your zazen. That’s all we have to do!
> 
> If you feel hungry, all you have to do is just eat. And then *after* eating you can very naturally see something. But *before* you eat, you cannot expect a full stomach, because you [haven’t eaten] yet. So all you have to do is, you have to eat. 
> 
> But intellectually you have to know: what is zazen, what is the purpose, what’s the meaning of zazen, et cetera. So that’s why we have to explain: how to do zazen, how to eat breakfast, how to eat supper, et cetera. But when you jump into the activities, [jump] with the full functioning of your intellectual sense, and just eat. 
> 
> It’s not just eat *blindly*. With your *full* attention, your full kindness – then you eat. And then very naturally, you can see something else. 
> 
> So, that is zazen. But usually we always expect something *before* you do zazen, [we expect something] *from* the zazen. Don’t you think so? So always your mind is spinning: “What is zazen? What’s the purpose of zazen?” If you do zazen, you have heard something about zazen from your friends or from books: “Zazen makes you calm.” So very naturally when you sit in zazen you expect the calmness. But actually your mind is busy! It’s pretty hard to find the calmness. So you are confused very much!
> 
> So calmness or not calmness, that is an intellectual understanding, temporarily. “What is zazen? What is the purpose? What do you mean?” Et cetera. “Why do we have to do this?” Many reasons there. But when you start to do zazen, *forget those explanations and just sit*. 
> 
> There are three points we have to follow in zazen: harmonizing body, harmonizing mind, harmonizing your breath. So, let me show [you] first how to do zazen. And then after that, I will explain a little bit. 

We do this by harmonizing the breath, harmonizing the mind. 

“nothing whatever to do with sitting or lying down” probably means we must carry this to *all* aspects of our lives – just do our sitting, but don’t get carried away by the result. 

> And next, harmonizing the breath, harmonizing the mind. This is also very important. 
> 
> External physical condition or internal physical condition – the human body is characterized by sort of *homeostasis*. So harmonizing your breath, harmonizing your mind, that is exactly keeping the function of your brain stem completely in balance, creating a strong feeling of being present right-now-right-here. Because the central nerves [are] working pretty well, and also the frontal lobe, the cerebral cortex, really rests perfectly. When the cerebral cortex rests... if you can make it rest, well, it works very naturally, smoothly, without giving any pressure to the central nerves. So central nerves and your brainstem and cerebral cortex and all things work pretty well; so very naturally, the function of the hormones [works] pretty well, breathing [goes] pretty well. And then very naturally, the mind blooms: so-called *tranquil*. So very naturally, you really feel strongly or stably *being present*, right-now-right-here.
> 
> On the other hand, when the external or internal physical condition operates pretty well, at that time you can create *vitalities*, you can feel really strong vitalities. 
> 
> So two things you can realize through this practice. You can feel exactly being present: completely beyond *you like* or *you don’t like*, just being present. You can notice this through this sitting. On the other hand, you can realize vitality. You want to *live*, you want to be present; that is vitality. 
> 
> Two things come up. So sometimes you don’t know what to do. Strong vitality comes up, energy comes up. *[He laughs.]* But at that time, don’t worry, don’t worry. Just let it go. Just... be with it. If you poke your head into something *extra*, something particular – vitality, energies – [either] depressing energies or strong energies, et cetera – that is a problem for you. So don’t worry. Whatever kind of energy comes up, all you have to do is just sit continually, keeping balance. 
> 
> So very naturally your whole body and mind is characterized by homeostasis, constantly keeping balance. That is influencing your life. And also you can fit your life into human society through this experience. So you bring your body and mind into human society, but your mind and body are very calm and keeping balance. And also, [...] you help somebody with this situation of your body and mind, even if you don’t say [anything]. 
>
> So when you join human society, still you can really experience this feeling of being present stably and securely; on the other hand, [there is] a feeling of desire to be present. Both. But both are completely working in equality. So that is keeping balance; exactly keeping balance. 
> 
> You cannot always keep calm... because you have to act! Even if you sit down, it is acting. Even if you don’t say anything, it is acting. In order to act, you need vitality, energy. Don’t you think so? So, both. But both don’t interrupt each other; [they are] exactly keeping balance. This is characteristic of your bodies, externally or internally. That is called *homeostasis*. Completely. 
> 
> Let’s keep this function, characteristic of your body and mind like this. 
> 
> *[Tape break.]*
> 
> You can help people like this, and also you can help yourself like this. So very naturally you can really enjoy yourself. 
> 
> At that time, still [there] is a problem: so-called *egoistic*. “I am a great man” – like this. That is ego. It’s ego. Or, there is a very strong desire: “I want to keep this. I want to be a good boy, wherever I am, so I want to do zazen.” So sometimes [you] kick out anybody who interrupts you; [you kick them] out and [say], “I want do zazen.” You don’t care about family, you don’t care about school, you don’t care about the office. Sometimes you really want to do it. This is egoistic, in a sense.
> 
> The more you realize how wonderful the function of homeostasis [is that] you can realize, it becomes selfish. So finally, all you have to do is: forget it! *[He chuckles.]* All you have to do is, day by day, just keep this practice. Just, on and on. Without expectation [of] anything. Just keep it. 
> 
> That is a religious practice. *[He chuckles.]* Okay? 
> 
> But before this, if you attach to the good aspect of your experience through zazen, at that time you create a certain expectation through the zazen. “Enlightenment! More, more, more!” Desires going endlessly. At that time, you cannot become peaceful, because [you are thinking], “More, more! Better life, better life!” It keeps you busy. So [where] is the peace? In zazen you are confused; you are not in peace. 
> 
> Zazen is exactly [a symbol of] peace. Exactly. That means around the zazen, [there is] nothing to touch [the] zazen; only zazen is standing there. That’s all! But if you really realize how *wonderful* zazen is, you are exactly creating desire to experience something more: “I want to be a good boy,” “I want to help people,” “I want to do zazen more,” “I don’t care about human problems”... *[he laughs]* Always those things come up. And then very naturally [you ask], “How many hours should I do it, in order to get the ‘good boy’”? So very naturally it goes on and on, desires coming up. Don’t you think so? So where is the peace? You are completely doing the same things as you usually do. 
> 
> But why do you do zazen? I don’t know why – but [it’s] because consciously or unconsciously you want to be peaceful, don’t you? *[He laughs.]* Well, even if you don’t know, unconsciously or consciously you want to be present in peace and harmony, right now, right here. That’s all you have to do. For this, why don’t you just sit?
> 
> So [...] all you have to is harmonize your mind, and body, and breath. And then you can realize the two feelings. [First:] being present, exactly. Beyond your like or dislike, you really appreciate your presence, realizing how valuable you are, [how valuable] your presence is. Second: strong vitality comes up, constantly. Both don’t bother each other; [they are] exactly keeping in balance. That is called peace, or tranquility. This is really helping people, and helping you. 
> 
> But at that time, if you expect these rewards from zazen, it is exactly not religious practice, it is just like the same things as you do in your everyday life. Do something, and then what? Do something, and then what? I get [the two] good things, and then what? Always *what*, *what*, *what*? That keeps you busy. In a sense, it’s fun, but in a sense, it’s a cause of trouble. So you never find peace. 
> 
> But zazen is exactly to realize *who you are*. Not losing the energy, not losing the vitality, not losing yourself as you really are. That’s all you have to do. That is important for us. For this: whatever you experience, forget it! Okay? All you have to do is to carry it forever; just like the water of the Ganges river: just going. That is really great power, supporting your life, behind your life. You don’t see it – but it’s really great help. That is called security: *spiritual security*. 
> 
> But in the human world always we can see [some result]: if you do something, then you can get [some] power. Mentally or physically or materialistically, you can get power. But that [kind of] power is always [that] you get the power [and] next moment it disappears. Don’t you think so? Always it disappears. And then next you can get more; and next moment it disappears. *What are you doing*, finally?
> 
> But zazen is not like this. 
> 
> So wherever you can get power, physically or mentally: that’s fine. Don’t worry about that. All you have to do is just carry the zazen, just like this. Through which you can get any kind of powers. You can get it, but the power you can get is not important; that is secondary. Helping so much... [well,] you can get it. But don’t worry about this, don’t hang around this. Appreciate it! Appreciate those experiences. But don’t hang around. All you have to do is just to carry your zazen. That means experience that perfect harmony. You can experience harmony, and you can help others, and you can help *you*. 
> 
> And then Dōgen Zenji says finally, “This experience should be shared with not only your friends, [but] all sentient beings.” Anyway, give it to all sentient beings. So – why should I keep it? *[He laughs.]* All I can keep is just zazen. So whatever I can have, share it with all sentient beings. Give it. And then, that is a great practice for us. Very naturally you can get [real] power, behind the power you can see. That is called *personality*; spiritual security. That is deepening your life. 



The general idea of this line appears in too many Katagiri Roshi talks to cite. 



```{=typst}
#pagebreak()
```

# Chapter 16: Steady, Immovable Sitting

## Paragraph 6 and Paragraph 7 Part 1

> 尋常坐處、厚敷坐物、上用蒲團。或結跏趺坐、或半跏趺坐。謂、結跏趺坐、先以右足安左腿上、左足安右腿上。半跏趺坐、但以左足壓右矣。寛繋テ衣帶、可令齊整。次右手安左足上、左掌安右掌上。兩大拇指、面相拄矣。乃正身端坐、不得左側右傾、前躬後仰。要令耳與肩對、鼻與臍對。舌掛上腭、唇齒相著。目須常開。鼻息微通。身相既調、欠氣一息、左右搖振。兀兀坐定、思量箇不思量底。

> At your sitting place, spread out a thick mat and put a cushion on it. Sit either in the full-lotus or half-lotus position. In the full-lotus position, first place your right foot on your left thigh, then your left foot on your right thigh. In the half-lotus, simply place your left foot on your right thigh. Tie your robes loosely and arrange them neatly. Then place your right hand on your left leg and your left hand on your right palm, thumb-tips lightly touching. Straighten your body and sit upright, leaning neither left nor right, neither forward nor backward. Align your ears with your shoulders and your nose with your navel. Rest the tip of your tongue against the front of the roof of your mouth, with teeth together and lips shut. Always keep your eyes open, and breathe softly through your nose.
>
> Once you have adjusted your posture, take a breath and exhale fully, rock your body right and left, and settle into steady, immovable sitting. [SZ] 
 
> At the site of your regular sitting, spread out thick matting and place a cushion above it. Sit either in the full-lotus or half-lotus position. In the full-lotus position, you first place your right foot on your left thigh and your left foot on your right thigh. In the half-lotus, you simply press your left foot against your right thigh. You should have your robes and belt loosely bound and arranged in order. Then place your right hand on your left leg and your left palm [facing upwards] on your right palm, thumb-tips touching. Thus sit upright in correct bodily posture, neither inclining to the left nor to the right, neither leaning forward nor backward. Be sure your ears are on a plane with your shoulders and your nose in line with your navel. Place your tongue against the front roof of your mouth, with teeth and lips both shut. Your eyes should always remain open, and you should breathe gently through your nose.
>
>  Once you have adjusted your posture, take a deep breath, inhale and exhale, rock your body right and left and settle into a steady, immobile sitting position. [EB]

## Commentary

> And next, the *movement system*. 
> 
> The movement system comes from the unity of your physical and mental organs. Your body and mind work, and then simultaneously movement comes up. 
> 
> You cannot destroy your movement. Sometimes movement comes from instinct; sometimes it comes from the sensory world; sometimes it comes from a higher level [of spirit]. Sometimes, we don't know. Karma. But anyway, there is always movement. 
> 
> So we have to make arrangement of movement. For this, Dōgen Zenji says, that is the half lotus position or full lotus position. Or he says: 
> 
> > Place both your hands in this manner, close to the body, with the joined tips of the thumbs opposite the navel.
> 
> Or, 
> 
> > Sitting upright in proper position, neither inclining to the left nor to the right; leaning neither forward nor backward.
> 
> > Sitting in zazen silently and immobile.
>
> This is very simple movement. The two hands are unified. Your eyes are not wide open, not closed, just *[unintelligible]*. That is unification of the movement of your eye-nerve system. If you open your eyes wide, it really distracts your mind. So not wide, not closed. And two hands put together, lips together, and teeth together; the tongue should be touching the roof of your mouth. And full lotus or half lotus. Just sit down; not leaning forward, not leaning backward, just straight up. 
> 
> This is the movement simplified by our arrangement. 
> 
> – From  [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 1” (39:42)](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1#3942).

“Settle into steady, immovable sitting” might be translated as “sitting in zazen silently and immobile” (see [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 1” at 39:42](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1#3942)). Here *immovable* or *immobile* has a meaning beyond simply staying still physically, because mind and body are closely connected.

> And also there is the regulation of the body: so we have to have full lotus or half lotus position, and hands in the position of the *mudra*. And also, finally, we have to sit in the proper way, *immobile*. 
>
> Even though you sit quietly, your body is always shaking and moving, because there is a certain gap between zazen and you. That is what is called *suki* (隙) in Japanese, [...] a crack, or a [pivot]; a crack between the two objects. Immediately you can see mental or psychological agitation, so mental or psychological agitation immediately becomes the physical wave. That’s why if you sit quietly, you don’t see [it], but actually you always move. 
> 
> So, sit in the proper way, *immobile*. And *immobile* means *just sit* physically, and also mentally, psychologically, you must be completely one with sitting. 
> 
> Because if you have a mental, psychological gap, slip, or crack between two objects, you and zazen, it means that when attention slackens, certain signs of laxity appear. That is called *suki*, or crack [...]; and then immediately, your body is moving. So that means it’s not *real* zazen. The continuity is broken up; at that time, you can create *suki*. That is mental or psychological agitation. 
> 
> That’s why we have to do zazen with what? Not with the mind first, but with the body. Legs, hands, and the whole body. But [the body] is very closely related related with mind, number five. That’s why if there is [a] mental, psychological crack, the body shows something.
> 
> So if you do zazen, immediately that is really closely connected with number six, [total personality]. Because if you become one with zazen physically, there is no [design] of oneness between zazen and you. Very naturally, there is no [design] of concentration. That means you are connected with number six: manifestation of *total personality*. You can manifest very naturally. 
>
> That’s why we do zazen physically first.
>
> – From [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 2”](https://katagiritranscripts.net/1979-06-10-Fukanzazengi-Talk-2).



> Proper physical posture means to keep your body balanced. If you have this straight posture like this, that is exactly that you keep your body balanced, externally, physically. And simultaneously that’s connected with the nervous system, the brain stem. Central nerves and spinal cord are exactly connected. So if you have a proper posture physically, that means exactly the function of the brain stem works and keeps in balance. That’s exactly [what it] means. So that’s why sitting in proper posture is important. 
> 
> So if you’re sitting like *this*, *[demonstrating a posture]*, you cannot sit for long, and also you cannot really concentrate on the sitting. If you sit like *this*, which means too comfortable posture for you *[he laughs]*: at that time [you are] thinking, thoughts are coming up. So it’s very difficult to become sort of tranquil. 

Katagiri Roshi discusses zazen posture in much more detail in his zazen instruction:

> [...] For [zazen], we use these round cushions. If you don’t use a round cushion, very naturally the center gravity is around the hips. So if you fall asleep, you fall down, like this. *[There are some chuckles.]* Because this posture is very unstable. If you sit like this it seems to be comfortable, but it’s not comfortable as a whole. Because you oppress your intestines, so your intestines don’t work, you know? And also your heart is oppressed, so you cannot breathe well. And also if you cannot breathe well, then very naturally your nerves become irritated, and your hormones cannot keep balance. So very naturally as a whole you become irritated, so you cannot sit for [very long]. 
> 
> So even if you [feel] uncomfortable sitting straight, this is pretty good for us. Because if you straighten your back and front, very naturally all your organs operate very well. 
> 
> So we use these cushions. If you use this cushion, very naturally this zazen forms a three-dimensional triangle, and then the center of gravity is right in the middle of this triangle. It makes your posture very stable. So even if you fall asleep in zazen, you cannot fall. So while you do zazen can sleep well, very naturally - just like this. *[Laughter.]* 
> 
> So that’s why we do this posture. And also there are two postures: half-lotus – this is half-lotus. Or vice-versa: your left leg on the right side. This is the half-lotus. And also full-lotus is like this: both your legs up on your knee. 
> 
> And then, if you do this posture, your weight is put on the three points: two knees and the hips. Two knees on the square cushion, and the hips on the round cushion. So, this is the posture. Posture is very important. 
> 
> Next, put your hand palm upward on your knee. Then, take deep breaths. Open your mouth just slightly. Let the breath in through your mouth, and when you inhale your body is arching backward a little bit, stretching the front. Very slowly, with full attention, okay? And then when you exhale, your body is arching forward, just like taking away all the inhaled breath from the lower abdomen, just arching forward. Do you understand okay? Let’s repeat this one. 
> 
> And then next, lean to the right as you exhale, stretching out the left side of your body. And bring your body back to the center as you inhale. And exhale while leaning to the left, stretching out the right side of your body. And inhale and bring it back to the center. Let’s repeat this [...] And the motion goes from large to small. This is a very important practice before you sit. This is a preparation for your sitting, physically and mentally. 
> 
> And then next, your left hand, palm upward, is placed on your right palm, and the thumbs just touch each-other, right above your middle finger. Not forward, and not backward: right above the middle finger. Making the form of an ellipse – not a circle, not a square. Like this. Not a loose feeling, not tense. A very soft, gentle form you should make. 
> 
> This is called the *cosmic mudra*. This is the symbol of the cosmic universe. We cannot exist without the universe, so we should appreciate the universe. To appreciate the universe means you should do something *with* the universe, physically and mentally. So why don’t you show the universe? But a universe is *big*! But we can know the characteristic of a universe: to unify two beings, together, in peace, in harmony. So that’s why two hands are put together like this. 
> 
> And this is the universe. So if you believe this symbol of the universe made by your hands – well, that symbol really works. But if you don’t believe, the symbol is just a symbol. It doesn’t work in *you*. 
> 
> Just like the American flag. If you see the American flag, you stand up and you do this, and then the symbol of American flag works with you. Do you understand? The same applies to this. This is a symbol, but a symbol is not a symbol, a symbol is something which should [be] alive in you – when you *make* it alive, when you use it. At that time, the symbol really works. But a symbol itself doesn’t have any sense. So only when you use it, it really works. 
> 
> So anyway, that’s why we make a universe with two hands. And then the universe must be one with you, with the center of gravity. That center of the gravity is always lower abdomen, so this universe must be touched to the lower abdomen. 
> 
> And the thumbs are placed a few inches below the navel: not too high, not too low. 
> 
> And your arms go forward a little bit – not *too* much, like this, not [touching] the side of your body. So go a *little* forward. Just like holding raw eggs under your arm: neither crush, nor drop. Okay? And then very naturally your arms relax.
> 
> Next, in the lower back, push it forward, a little hard, and [adjust a little]. This practice is a little hard for you, because you have never done it before. So if you do zazen like this, next day you [may] have a sore back...
> 
> *[Recording interruption.]*
> 
> ... you are alive, anyway, and you body, your mind is working very normally. [Sorry,] don’t worry about this. 
> 
> So, push the lower back first, and [adjust a little]. And [straighten] your back, and upper back, and your head, and keep your neck in parallel with the wall, first. And then, without moving your neck, pull your chin in, [so that you] feel like [you’re] pushing the ceiling with the top of the back of your head. And then very naturally your back becomes taut, just like sticking a straight stick from the top of your head to the bottom. 
> 
> And then, very naturally your eyes [are] cast on the floor, and looking at a certain point on the floor – a little wide area. Don’t pick up *[unintelligible]* from the floor; just cast down your eyes. And then this area is almost in the same distance as your sitting height. So very naturally your eyes open just slightly – not wide, not closed. If you close your eyes, you really enjoy innate visualizations, [so it seems to you to create some trouble]. If your open your eyes too much, that is also trouble: your mind scatters. So not wide open, not closed. But in the beginning of zazen if it is difficult to take care of your mind, at that time you can close your eyes – for a while. Okay? For a while. And then as soon as possible, you should open your eyes. 
> 
> So let’s have this posture, and cast down your eyes on the floor, your eyes open just slightly. And at that time, your nose and navel are in a vertical line; and ears and shoulders in the same straight line. That means you cannot lean forward, you cannot lean backward. You cannot lean to the right or to the left. Exactly straight up. Just like a mountain. 
> 
> This posture really teaches us a middle way. Exactly [a] middle way: neither attaching to the right or to the left, regarded as two extremes, ideas. Not to the right or the left, not front or back: just straight in the center. That means the Middle Way. But the middle way is not going in the middle, but we know *both*; all situations. And *then* you can walk in the middle. 
> 
> So you have to keep your body always not tipping forward, or leaning backward, or leaning to the right, to the left. You have to watch. You have to understand the *whole* situation there.
> 
> And then next, bring your teeth together, and lips together. And also your tongue should be touched to the roof of your mouth, as natural as you can. And very naturally your mouth is closed. 
> 
> Next, let the breath in through your nose, and let it go down to the lower abdomen. And let all the inhaled breath out through your nose, slowly. 
> 
> Okay, let’s repeat this breathing. 
> 
> When you have a proper posture physically, very naturally your breathing is going in and out, from your nose to the lower abdomen, without stopping on the way to the lower abdomen. 
> 
> That is the breathing.
>
> If you pay attention to the breath, the rate of the breathing, respiration, becomes a little bit slow. Not too slow, not too fast – but if you pay attention to your respiration, the respiration goes a little bit more slowly than as usual. 
> 
> Sometimes you have a problem for your breath. At that time, let it go, as naturally as you can, for a while. Just breathe naturally for a while, if you have a problem. [Like] stomach pain, because you pushed the breath too much to let it go down to the lower abdomen; at that time sometimes you have too much tension on the lower abdomen. Or sometimes you cannot breathe well. So at that time, let it go, and breathe as naturally as you can, for a while. 
> 
> Don’t worry about [whether a breath is a] good breath or bad breath. Don’t worry about this. Don’t worry about judgement. If you see a not good situation of your breath, let it go for awhile, and take care of this situation of your breath to return to normal. But if you are irritated, [trying] to control your breath, at that time you make more [of a] problem. So sometimes you can control [it], but sometimes you cannot control [it]. So if you cannot control [it], for a while let it go, then see what is the problem. You can do [this].
> 
> Breathing is always changing. You cannot keep a certain pattern of your breath. Constantly changing – according to your emotion, according to your feeling, and also physical condition, and also external circumstances. [And] internal circumstances – body too. Always changing. 


```{=typst}
#pagebreak()
```

# Chapter 17: The Essential Art of Zazen

## Paragraph 7 Part 2

> 不思量底、如何思量、非思量、此乃坐禪之要術也。  

> Think of not thinking, "Not thinking --what kind of thinking is that?" Nonthinking. This is the essential art of zazen. [SZ] 

> Think of not-thinking. How do you think of not-thinking? Non-
thinking. This in itself is the essential art of zazen. [EB]

## Commentary

- insert the story from zazenshin (?) here. see EB

> These words derive from the following dialogue, which is the central subject of SBGZ zazenshin:
>>  A monk asked Yüeh-shan, "What does one think of when sitting immobilely in zazen?"  
>>  Yüeh-shan replied, "One thinks of not-thinking."   
>> "How do you think of not-thinking?" asked the monk.   
>> "Non-thinking," answered Yüeh-shan.
>
> – From [EB]


Here is body, breath, and mind, and also no-mind.

> That’s [also] why in *Fukanzazengi* [Dōgen says],

> > Zazen must be deportment beyond one’s hearing and seeing.

> But, of course it is hearing and seeing, because you cannot move even a single mote of dust, nor infringe upon a single phenomenon. So finally you can manifest the beautiful flower of the total personality right in the middle of zazen. At that time, “Is it not a principle that is prior to one’s knowledge and perceptions.” And you have to use knowledge and perceptions – not *no-mind*. “No mind” means through and through, you have to use mind. So, that is the practice of regulation of your body, breath, and mind. 
> 
> We should know the mind is very picky; “monkey mind.” That’s why we need the practice of regulating the mind. But we have to *use* the mind. When you regulate your body and breath, there must be the mind *with* your body, your breath. Otherwise, you become [like] cats and dogs. Cats and dogs and birds can do with their bodies but no mind. But we are human beings. So first we have to do something with our body, but there must be mind, constantly. 
> 
> So, the final goal of regulating the mind is to be free from mind, because mind is picky. That’s why Dōgen Zenji says we have to practice samadhi, complete samadhi, becoming one; using your whole body and mind in order to fit your object perfectly. Adjusting, regulating your body and breath and mind. And then, if everything is perfect, at that time very naturally your body fits to your object, and then, something happens. Something happens; we don’t know what it is. And then when we see it, when our mind is immediately there and *picking* that, then we say, “Oh, that’s zazen.” But before your mind picks it up, that zazen is *no-name*. Just, something happens. So, very naturally, zazen blooms. And also *you* bloom, as total personality there. 
>
> 

Nonthinking as the essential art of zazen is the same as shinjin datsuraku and “dullness and distraction are struck aside.” It all ties together.

> So *sanzen* is *zazen*. How can you surrender to simplicity in life? Dōgen Zenji [says], that is zazen. 
>
> And then he says zazen is *shinjin datsuraku*, that means “casting off body and mind,” in other words “dropping off body and mind.” Or, he says, “Dullness and distraction are struck aside from the beginning.”
> 
> Dullness and distraction are not something you try to remove. If you try to remove [them], you create more distraction and dullness. Because dullness and distractions are something that [is] created, produced, by your attitude, by your actions, activities – so, according to [...] conditional elements, conditional circumstances. So you don’t know how to be free from [them]. No matter how long you use techniques – psychologically, philosophically, or scientifically – you never get freedom from dullness and distraction. The moment when you feel freedom from dullness and distraction, immediately you are confused right in the middle of freedom of dullness and distraction. That’s why human beings constantly seek for the psychologist to let you be free from dullness and distractions, you know? You always feed the psychologist. *[He laughs.]* 
>
> So at the dropping off body and mind if you do zazen, simultaneously the dullness and distractions are struck aside from the beginning. This is a key point of zazen. That’s why Dōgen Zenji [says] “This is the essential art of zazen.”



In Katagiri Roshi’s Zazen instruction, this is part of harmonizing the mind:

> And then next, the mind. Harmonizing your mind. The mind is really busy – like a monkey. So take care of your mind. 
> 
> [Harmonizing your] mind should be: let your mind sit in zazen with you. Constantly. 
> 
> Don’t let it go. If you let it go, it runs wild. 
> 
> Anyway, let whatever kind of mind – monkey mind, or good mind, or calm mind, whatever it is – let your monkey mind sit together with you. That is a point. 
> 
> So for this, your mind should be with your breath. 
> 
> For this, when you inhale, maybe you can concentrate on [the] lower abdomen going out, and when you exhale, you can concentrate on the lower abdomen going in. Or, you can do the reverse. When you inhale, your lower abdomen goes *in*, and when you exhale, your abdomen goes out. Can you do this? This is a little bit “unusual” way *[he chuckles]*: usually when you inhale, the lower abdomen goes out, when you exhale, it goes in. [You can do it] either way. Particularly when you feel sleepy or when you’re really lazy and [...] losing the spirit, at that time practice a little bit breathing [where] you inhale and your lower abdomen goes in, a little bit, and [it’s] a little slow. And when you exhale, the lower abdomen goes out. This is pretty good. It wakes you up. Sometimes. *[He chuckles.]* So a little slowly – particularly when you exhale, a little more slowly. 
> 
> This is the breathing. It’s pretty good practice. Either way. 
> 
> Always your mind must be with the breath. But mind goes, immediately. So at that time, [take] it back. Bring it back to your zazen. 
> 
> But very often, your mind is just like a wild kid. A really wild kid. Always he is screaming, and going out. And you are just like a mother; always [taking him] back.
> 
> I don’t know how often you should take him back to your zazen. Maybe your whole period of zazen, you always see the mind going out, and take him back, and going out, take him back – always. So finally you say, “What *is* zazen?” You don’t understand zazen’s meaning. But that’s alright, that’s alright... don’t worry. All you have to do is see the mind: where is it? And then if it goes, take it back, with your best. That’s all we have to do. 
> 
> – From Katagiri Roshi’s Zazen Instruction

- search for “not thinking”

> In other words, I mentioned before, bodhisattva can realize the truth that recognition of the calmness is not perfect calm. This is a vibration, very subtle vibration of the mind. But how can you be free from this fine vibration, minute vibration of the mind? Which bodhisattva recognizes that his calmness is not perfect calmness. In other words, because perfect calmness is not something you can see objectively. Even slightly, there is some space between you and calmness, this is already dualistic. The perfect calmness is you must be exactly one with calmness. At that time, there is no opportunity to see or to know objectively. So it's very difficult to know. No chance, no opportunity to recognize perfect calmness when you are in calmness. No. 
> 
> So, how can you be free from the very minute vibration of the mind? No chance. No opportunity. By dualistic sense, no, no way to be free from. 
> 
> So there is no way to be free – no technical, no dualistic way to be free from this minute vibration of the mind. No. So finally, what you can find, the unique way of being free from this very minute vibration of the mind is, you just stop vibrating. That’s it. It means you put yourself right there. That's it. So very naturally, finally, any kind [of] Buddhism always says, “don't do it.” When you suffer from delusion during zazen, how can I be free from thoughts and et cetera? Stop it. That’s it. Instead of the expression of stopping the thought, thinking, a Zen teacher says, let the thinking do zazen with you.
> 
> In other words, stop the thinking of being free from thinking or not thinking. Completely stop it. So all you can do is just do zazen.
> 
> That's it. No technical way, how can I be free from delusions.
>
> 1986-03-14-Awakening-of-Faith-Talk-34




For “the essential art of zazen,” see [“Zazen: Entry to the Buddha Dharma” at 18:32](https://katagiritranscripts.net/1987-03-07-Zazen-Entry-to-the-Buddha-Dharma#18:32): “... zazen is *shinjin datsuraku*, that means ‘casting off body and mind,’ in other words ‘dropping off body and mind.’ Or, he says, ‘Dullness and distraction are struck aside from the beginning.’ ... So at the dropping off body and mind if you do zazen, simultaneously the dullness and distractions are struck aside from the beginning. This is a key point of zazen. That’s why Dōgen Zenji [says] ‘This is the essential art of zazen.’”

-- But wait – this is the “think not thinking” section! 

Still, somewhere we have to include the “ah!” part. 


“Don’t think anything” is “think not-thinking”: see [“*Diamond Sutra*, Talk 8: Provisional Being”](https://katagiritranscripts.net/1979-07-25-Diamond-Sutra-Provisional-Being”).

For *shujo shin* (“one-mind”) as *non-thinking*, see [“*The Awakening of Faith* – Talk 33”](https://katagiritranscripts.net/1986-03-07-Awakening-of-Faith-Talk-33).

- look up non-thinking as “Ah!”

```{=typst}
#pagebreak()
```

# Chapter 18: The Dharma Gate of Joyful Ease

## Paragraph 8 Part 1

> 所謂、坐禪非習禪也、唯是安樂之法門也、究盡菩提之修證也。  
  
> The zazen I speak of is not meditation practice. It is simply the dharma gate of joyful ease, the practice realization of totally culminated enlightenment. [SZ] 

> The zazen I speak of is not learning meditation. It is simply the Dharma-gate of repose and bliss, the practice-realization of totally culminated enlightenment. [EB]

## Commentary

習禪 is *shūzen* “practicioner of dhyāna” see *Treasury of the True Dharma Eye: Dōgen’s Shōbōgenzō, Volume 8*, by the Sōtō Zen Text Project.

The glyphs 13i# (shuzen) are an abbreviation of the expression "to practice dhyana" (shujù zenna 1273i#J) and are also translated herein as "the practice of dhyāna." In both the Indian and the East Asian contexts, the term "dhyāna" is used in two ways: 1) A narrower sense, in which it refers specifically to successive stages of mental absorption, or trance, known as the four dhyānas (shizen i#); and (2) a broader sense, in which it includes both the inducement of mental calm (shi It; S. śamatha) and the cultivation of insight (kan #I; S. vipaśyana).

In the literature of Zen, "practitioner of dhyāna" is a term of disparagement for monks who specialize in various forms of meditation theory and practice but do not understand that what Bodhidharma transmitted to China was not merely dhyana concentration (zenjo i#E), i.e., the fifth of the six perfections (roku haramitsu kittiti; S. şad-paramită), but rather the awakening of Buddha Sakyamuni — the buddha mind (busshin 1# L) — itself.

vipassana is *kan* 觀

The “dharma gate of repose and joy” or “dharma gate of repose and bliss” is discussed in [“Bendōwa: Dōgen's Questions & Answers – Talk 3”](https://katagiritranscripts.net/1987-03-13-Bendowa-Talk-3) at [55:17](https://katagiritranscripts.net/1987-03-13-Bendowa-Talk-3#5517) and [1:11:57](https://katagiritranscripts.net/1987-03-13-Bendowa-Talk-3#11157).

```{=typst}
#pagebreak()
```

# Chapter 19: The Koan Realized

## Paragraph 8 Part 2

> 公案現成、籮籠未到。若得此意、如龍得水、似虎靠山。  

> It is the koan realized; traps and snares can never reach it. If you grasp the point, you are like a dragon gaining the water, like a tiger taking to the mountains. [SZ] 

> It is the manifestation of ultimate reality. Traps and snares can never reach it. Once its heart is grasped, you are like the dragon when he gains the water, like the tiger when he enters the mountain. [EB]

## Commentary

“The koan realized” (公案現成) is the same characters as *Genjōkōan* (現成公案), only in the order “*kōan genjō*.” For the meaning of *genjō* and *kōan* see [“*Genjōkōan*: Talk 1” at 42:48](https://katagiritranscripts.net/1987-06-06-Genjokoan-Talk-1#4248). See also [“*Gabyō*: Painting of a Rice Cake – Talk 1” at 43:27](https://katagiritranscripts.net/1986-12-01-Gabyo-Talk-1#4327) for *genjō* as “actualization or manifestation in the immediate present” or “subjectivity.” 

- “traps and snares” see again 1987-03-12-Bendowa-Talk-2


```{=typst}
#pagebreak()
```

# Chapter 20: Dullness and Distraction Are Struck Aside

## Paragraph 8 Part 3

> 當知、正法自現前、昏散先撲落。  

> For you must know that the true dharma appears of itself, so that from the start dullness and distraction are struck aside. [SZ] 

> For you must know that just there [in zazen] the right dharma is manifesting itself and that from the first dullness and distraction are struck aside. [EB] 

## Commentary

This line is extensively discussed in [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 1”](https://katagiritranscripts.net/1979-06-09-Fukanzazengi-Talk-1) as “a sort of conclusion of the main subject in *Fukanzazengi*,” and as “[the real] meaning of *shikantaza*.”

“Dullness and distraction” are meant to exemplify all kinds of delusions. See [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 3”](https://katagiritranscripts.net/1979-06-11-Fukanzazengi-Talk-3).

"Dullness and distraction" are extensively discussed in [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 3”](https://katagiritranscripts.net/1979-06-11-Fukanzazengi-Talk-3), and also [Talk 5](https://katagiritranscripts.net/1979-06-13-Fukanzazengi-Talk-5) and [Talk 6](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6).

This is synonymous with “body and mind of themselves will drop away.” See above.

```{=typst}
#pagebreak()
```

# Chapter 21: When You Arise from Sitting

## Paragraph 9 Part 1

> 若從坐起、徐徐動身、安詳而起、不應卒暴。  

> When you arise from sitting, move slowly and quietly, calmly and deliberately. Do not rise suddenly or abruptly. [SZ] 

> When you arise from sitting, move slowly and quietly, calmly and deliberately. Do not rise suddenly or abruptly. [EB]

## Commentary

> When the zazen is over, we release the posture of your hands. Put them on your knee, like this, palm upward. And move to the right, to the left, going from small motion to large. First drop down your head to the right shoulder as you exhale, and bring your head back to the center as you inhale. And drop down your head to the left shoulder as you exhale, and inhale and bring it back to the center. Let’s repeat. And the swinging is going from small motion to large. 
> 
> Your mind has been very quiet, so after zazen you cannot [move or] act roughly. That’s why this swinging must be going from small motion to large, like this.
> 
> And then release your posture of your legs, and stretch out. 
> 
> And then you can stand up. 


A practical example of moving calmly and deliberately appears in [“*Bendōwa*: Dōgen's Questions & Answers – Talk 2”](https://katagiritranscripts.net/1987-03-12-Bendowa-Talk-2) at [55:32](https://katagiritranscripts.net/1987-03-12-Bendowa-Talk-2#5532)

```{=typst}
#pagebreak()
```

# Chapter 22: Dying While Either Sitting or Standing

## Paragraph 9 Part 2

> 嘗觀、超凡越聖、坐脱立亡、一任此力矣。  
  
> In surveying the past, we find that transcendence of both mundane and sacred, and dying while either sitting or standing, have all depended entirely on the power of zazen. [SZ] 

> In surveying the past, we find that transcendence of both un-enlightenment and enlightenment, and dying while either sitting or standing, have all depended entirely on the strength [of zazen]. [EB] 

## Commentary

> Regardless of whether you are conscious of the truth or not, Buddhas and patriarchs constantly teach us there is a great function of existence, *the truth*. So constantly we have to say it, because the intent is that you will realize, sooner or later, that there is something transcendental. That means, there is a way to live, to show, to demonstrate, to manifest yourself as you are what you are, freely. This is development of human life, deepening your life. 
> 
> In other words, as I told you before: modern civilization is pretty good for us, and consciousness is pretty good for us, but we have to transcend the function of consciousness. 
> 
> *Transcend* doesn’t mean to destroy consciousness; *transcend* is to not attach to any [expected ideas]. We cannot say “consciousness is good” or “consciousness is bad.” *Transcend* means that through consciousness we should live in the best way, day after day. Think carefully, through and through, and then live in the best way. But – you cannot stay with your consciousness, by which you have lived in the best way. You must transcend your understanding, your best life. In other words, you should watch carefully your life, modern civilization, which we have created. That is really development of human life. 
>
> – From 1980-04-19-Blue-Cliff-Record-Case-3-Talk-1


Katagiri Roshi gave an entire talk with this line as the theme: [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 4”](https://katagiritranscripts.net/1979-06-12-Fukanzazengi-Talk-4). It begins like this:

> **Katagiri Roshi:** Toward the end of *Fukanzazengi*, as a conclusion, Dōgen Zenji explains how important *shikantaza* is from a different angle, from a various way. So, little by little, we try to learn this. [Dōgen writes,]
> 
> > In surveying the past, we find that transcendence of both unenlightenment and enlightenment, and dying while either sitting or standing, have all depended entirely on the strength of zazen.
> 
> The notes given by Professor Abe (Masao Abe) say about “dying while either sitting or standing”: 
> 
> > It is written in *Keitoku Dentō-roku* that Bodhidharma and the fourth, fifth and sixth Chinese Zen patriarchs died sitting in zazen, while the third patriarch died while standing under a large tree. Examples of both are common in the Zen histories.
> 
> So [according to] this point, some Zen teachers kept sitting and died. Some teachers died in sitting zazen, or standing under a tree, or standing on the platform while they were giving a lecture. Anyway, [there are] various examples from Buddhist history there. But it doesn't mean you should die in sitting or standing; it doesn't mean that. [The] point is how important shikantaza is, because they died in sitting, in standing, wherever they may have been; they died in peace and harmony. Whatever they did, wherever they were, they died.
> 
> Dōgen Zenji really wants to speak about how important zazen is. That zazen is shikantaza. In shikantaza, all delusions drop off from the first. That is “dropping off body and mind,” “body and mind dropping off.” That is zazen itself. 

Unfortunately there’s far too much material in the talk to include here.

```{=typst}
#pagebreak()
```

# Chapter 23: It Cannot Be Understood by Discriminative Thinking

## Paragraph 10 Part 1

> 況復拈指竽針鎚之轉機、擧拂拳棒喝之證契、未是思量分別之所能解也、  

> In addition, triggering awakening with a finger, a banner, a needle, or a mallet, and effecting realization with a whisk, a fist, a staff, or a shout --these cannot be understood by discriminative thinking; ... [SZ] 

> In addition, the bringing about of enlightenment by the opportunity provided by a finger, a banner, a needle, or a mallet, and the effecting of realization with the aid of a hosu (that is, a whisk), a fist, a staff, or a shout cannot be fully understood by one’s discriminative thinking. [EB] 

## Commentary

This is discussed in [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 6”](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6) at [21:38](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6#2138):

> I already told you a few stories so far. Dōgen gives lots of examples, but he didn’t explain concretely about each story. But the few stories I told you really [imply very well] the meaning of *shikantaza*, [which is] zazen based on body and mind dropping off. 
> 
> [Dōgen] says [in *Fukanzazengi*]: 
> 
> > In addition, the bringing about of enlightenment by the opportunity provided by a finger, a banner, a needle, or a mallet, and the effecting of realization with the aid of a *hosu* (that is, a whisk), a fist, a staff, or a shout...
> 
> Those things come from the old stories [of the exchanges] between the Zen masters and the Zen monks; [they are explained] in this book in the note. Overall it’s not [necessary to know]; I don’t have enough time to explain everything. That’s why I told you a few stories: Gensha Shibi’s, and one more I forgot. 
> 
> > ... cannot be fully understood by one’s discriminative thinking.
>
> We cannot understand *why* Gensha Shibi attained enlightenment by striking his toes and seeing the blood coming up. We don’t understand. *Why*? Does the blood have a mysterious power? I don’t think so. Blood is blood. Do his toes have a particular mysterious power? No. He didn’t use telepathy – just a rock. Rock is rock; it has no mysterious power. So why did he attain enlightenment? 
> 
> *[In the distance, the sound of a police siren starts.]* Because, I told you before, [without mind,] something happens with the rock, and toes, and the Gensha Shibis, and the *[unintelligible]* –– all are beings which are not associated with the mind. So everything exists, day after day, in the process of change, completely in the stream of change. *[The police siren is getting louder.]* Birds, zazen, and that siren: all things exist in peace and harmony, in the stream of change. And then something happens, according to [a] conditioned element, which will happen between the two. That conditioned element – *[the police siren finally stops]* – is characterized by one object, one being, used *perfectly* for another being, fitting into its object perfectly. This is conditioned element.
> 
> For instance: a sound comes up. Your ears hear the sound outside. When your ears [are] completely [used] perfectly, fitting into the sound, at that time you can hear. By what? Well, conditioned elements, which is called [*source*], *together-maker*. 
> 
> That conditioned element, from where does it come? We don’t know. We know it’s there. Well, according to Buddhist philosophy, that is called *dependent origination* – or *change*, constant change. The function of the conditioned element [is change], always, and *interdependence*: always connected. 
> 
> The sound is completely used for your ear, fitting into your ear perfectly. At that time, your ear becomes one with sound. And then, something happens. That [is] sound. At that time, that is *event*. 
> 
> And then immediately, mind associates with this siren, or your ear. And then, that is a gate. Which way would you like to go: this way, or that way? Very quick, very quick. And also, mind is very tricky. If you realize, “Hey, yes, mind is very tricky,” then you are already tricked. *[He laughs with the group.]* “I understand mind, how tricky mind is” – so you are already tricked by your understanding of how tricky mind is! So already, again and again, it is snowballing, first of all. 
> 
> Then finally what you have to do is: stop it. Stop it. How can you stop it? You cannot stop the mind. So the first important thing in order to stop the mind [is that] first your body must be used perfectly, fitting into your object. At that time, very naturally, mind stops. Can you [imagine]? Because your body and breath becomes one with zazen. At that time, your body is completely one with zazen. 




“The opportunity provided by” is omitted from the Sōtōshū translation, but this seems questionable. 

“Opportunity” is *ki* (機), which comes up again in “pivotal opportunity of human form”; see below. Other dictionary definitions of *ki* include “spring, trigger, motive, principle, potentiality, occasion” (see *The Heart of Dōgens’s Shōbōgenzō*, translated by Norman Waddel and Masao Abe, p. 12). For more on *ki* see [“Dealing with Death, Dealing with Life”](https://katagiritranscripts.net/1989-01-07-Dealing-with-Death-Dealing-with-Life).

```{=typst}
#pagebreak()
```

# Chapter 24: Deportment Beyond Seeing and Hearing

## Paragraph 10 Part 2

> 豈爲神通修證之所能知也。可爲聲色之外威儀。那非知見之前軌則者歟。

> ... much less can they be known through the practice of supernatural power. They must represent conduct beyond seeing and hearing. Are they not a standard prior to knowledge and views? [SZ]

> It cannot be fully known by the practicing or realizing of supernatural power either. It must be deportment beyond one’s hearing and seeing. Is it not the principle that is prior to one’s knowledge and perceptions? [EB]

## Commentary





This is discussed in [“*Fukanzazengi*: Dōgen's Universal Recommendation for Zazen – Talk 6”](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6) after [39:44](https://katagiritranscripts.net/1979-06-14-Fukanzazengi-Talk-6#3944).

> ... Using your body, perfectly fitting into your object. At that time, your body becomes one with zazen, zazen becomes one with you, very naturally. At that time, there is something that happens. That is called zazen. 
> 
> The [problem] is, mind attaches to it. That’s why Dōgen Zenji says, let’s practice regulation of the mind, no design of having reward. That is the [problem], so we have to understand *what is mind*. Very tricky mind, very “monkey” mind, always.
> 
> Well, we have to make every possible effort to do that, [because] we have a mind. Mind is already here; that’s why we have to practice. 
> 
> So Dōgen Zenji says, that’s why ... 
> 
> > ... it cannot be fully known by the practicing or realizing of supernatural power either.
> 
> Even though you can fly in the air, you cannot understand this kind of zazen, okay? *[He chuckles.]* 
>
> Or, Dōgen Zenji says,
> 
> > It must be deportment beyond one’s hearing and seeing.
> 
> If you see zazen *after* real zazen, that is an image of zazen, it is not real zazen. 
>
> *Deportment* means the behavior which is called zazen. In Japanese we call it *igi* (pronounced “ee-gi”, more or less). The *i* of *igi* means “majestic and awe-inspiring.” Very majestic. *Gi* of *igi* means fitting into, or mention of, the truth. That is form, your behavior. And that is deportment. Here it says “deportment,” but originally we use *igi*. Usually we use [the word] *behavior*, but that behavior is *igi* in Buddhism, because that behavior has a sense of majesty and also a sense of the awe-inspiring. [Your behavior is] fitting into the rhythm of the truth.
> 
> So, this behavior which is called zazen is completely beyond hearing or seeing through the six consciousnesses. Let’s return to conditioned elements, that’s all. 
> 
> Dōgen Zenji says, 
>
> > Is it not the principle that is prior to one’s knowledge and perceptions?
>
> That means that zazen, completely beyond hearing and seeing, is not a mysterious thing. There is still [...] being in accord with the function of knowledge and perception. How? Let’s use your body, mind, [and] breath. [They] are perfectly fitting into one object called zazen. 
> 
> At that time, something happens. And after that, mind associates, that’s all. Then mind says, “Ahh, *that’s* zazen.” And then you attach [to it]. But before mind, prior to the function of your mind, it’s really *just sit*. It’s a very simple practice.
> 
> That’s why Dōgen Zenji says, “Is it not a principle that is prior to one’s knowledge and perceptions?” It’s [there]. You have to [just] really *fit* into your knowledge and perceptions. 

```{=typst}
#pagebreak()
```

# Chapter 25: Intelligence or Lack Of It Is Not an Issue

## Paragraph 11

> 然則不論上智下愚、莫簡利人鈍者。專一功夫、正是辦道。修證自不染汙、趣向更是平常者也。

> This being the case, intelligence or lack of it is not an issue; make no distinction between the dull and the sharp-witted. If you concentrate your effort single-mindedly, that in itself is wholeheartedly engaging the way. Practice-realization is naturally undefiled. Going forward is, after all, an everyday affair. [SZ] 

> This being the case, intelligence or lack of it does not matter; between the dull and the sharp-witted there is no distinction. If you concentrate your
effort singlemindedly, that in itself is negotiating the Way. Practice-realization is naturally undefiled. Going forward [in practice] is a matter of every-dayness. [EB]

## Commentary

“Practice-realization” is again *shushō* (修證); see above. 

For a good look at the meaning of the term *undefiled* in Buddhism, see “*Blue Cliff Record* Case 52: Chao Chou Lets Asses Cross, Lets Horses Cross – Talk 1” (in progress). 

```{=typst}
#pagebreak()
```

# Chapter 26: Why Leave Behind the Seat in your Own Home

## Paragraph 12

> 凡夫自界他方、西天東地、等持佛印、一擅宗風。唯務打坐、被礙兀地。雖謂萬別千差、秪管參禪辦道。何抛卻自家之坐牀。謾去來他國之塵境。若錯一歩、當面蹉過。  
  
> In general, in our world and others, in both India and China, all equally hold the buddha-seal. While each lineage expresses its own style, they are all simply devoted to sitting, totally blocked in resolute stability. Although they say that there are ten thousand distinctions and a thousand variations, they just wholeheartedly engage the way in zazen. Why leave behind the seat in your own home to wander in vain through the dusty realms of other lands? If you make one misstep, you stumble past what is directly in front of you. [SZ] 

> In general, this world and other worlds as well, both in India and China, equally hold the Buddha-seal, and over all prevails the character of this school, which is simply devotion to sitting, total engagement in immobile sitting. Although it is said that there are as many minds as there are men, still they (all) negotiate the Way solely in zazen. Why leave behind the seat that exists in your home and go aimlessly off to the dusty realms of other lands? If you make one misstep you go astray from (the Way) directly before you. [EB]

## Commentary


- research “blocked”

- return to “thousand-foot pole” for focused zazen

```{=typst}
#pagebreak()
```

# Chapter 27: The Pivotal Opportunity of Human Form

## Paragraph 13 Part 1

> 既得人身之機要、莫虚度光陰。  

> You have gained the pivotal opportunity of human form. Do not pass your days and nights in vain. [SZ] 

> You have gained the pivotal opportunity of human form. Do not use your
time in vain. [EB]

## Commentary

“Pivotal opportunity” is *kiyō* (機要)  (Source: *Nishijima and Cross translation of *Shōbōgenzō*, Volume 1.) Katagiri Roshi discusses *ki* (機):

> I just use the term “momentum of time and energy”. We call in in Japanese “*ki*”. I think we chant the sutra at noon, the *Jijuyu Zanmai*, we call “*ki*”. The “*ki*” is “opportunity” – literally – or “device”, a piece of a device, like a machine. Or opportunity; opportunity is... well, time, you can create... not create, you can... how can I say. *Ki* is [that] you can create not only by you, you can create a *ki* by you and your object. Only both becomes one, and then you can create that *ki*. That is called “momentum”. 
>
> So momentum takes you to another momentum; you can’t stop it. That is human effort; we it call effort. Human effort is very pure, very pure – momentum. Even though you sleep, there is human effort there. Is that clear? That is called *ki*. 
>
> Or *zenki*, we call zenki “the whole works”. In the chapter of *Shōbōgenzō*, the title is “*Zenki*”; *zen* is “totality”. And Thomas Cleart says, “The Whole Works”. *Ki* means the same thing, [as I said]; *ki* means “opportunity”, “device”, or “momentum”... *working*. Momentum [of] time, momentum of energy. 
>
> From [“*Baika*: Plum Blossoms – Talk 2” (December 3, 1988) at 58:54](https://katagiritranscripts.net/1988-12-03-Baika-Talk-2#5854).

Katagiri Roshi also discussed *ki* in his final talk:

> When the totality appears in the actual [facets] of your life, at that time totality is called *ki* (機). In Japanese, *ki* means momentum. *Ki* means a kind of ... there are no English words, but *ki* is usually translated as *device*, or *work*, or *chance*, or *opportunity*. But still we don’t understand what *ki* means. 
> 
> Do you know the American TV series *Bewitched*? *[Laughter.]* I love it. *[Laughter.]* You know the woman, both the daughter and the mother, are witches. Do you know how the daughter always moves her nose? At that time, I always feel I want to *pinch* that nose before she does it. *[Laughter.]* The first moment of her nose moving, I want to pinch it, that’s what I am feeling. I am curious about that. That is called *ki*. *[Laughter.]* The whole works. In other words, you have to come back to the very first moment of your doing – gassho, or moving your nose, or zazen – and when you return to the very first moment, if you can grasp it, pinch it, that is called *ki*. That is a place where the dharma, wholeness, really works.
>
> – From [“Dealing with Death, Dealing with Life” at 33:32](https://katagiritranscripts.net/1989-01-07-Dealing-with-Death-Dealing-with-Life#3332).

```{=typst}
#pagebreak()
```

# Chapter 28: Emptied in an Instant, Vanished in a Flash

## Paragraph 13 Part 2

> 保任佛道之要機、誰浪樂石火。加以、形質如草露、運命似電光。倐忽便空、須臾即失。  
  
> You are taking care of the essential activity of the buddha-way. Who would take wasteful delight in the spark from a flintstone? Besides, form and substance are like the dew on the grass, the fortunes of life like a dart of lightning --emptied in an instant, vanished in a flash. [SZ] 

> You are maintaining the essential working of the Buddha
Way. Who would take wasteful delight in the spark from the flintstone?23
Besides, form and substance are like the dew on the grass, destiny like the
dart of lightning-emptied in an instant, vanished in a flash. [EB]

## Commentary

“Dew” and “lightning” are part of the famous verse at the end of the *Diamond Sutra*:

> As stars, a fault of vision, a lamp,  
> A mock show, dew drops, or a bubble,  
> A dream, a lightning flash, or cloud,  
> So should one view what is conditioned.  
>
> (From *Buddhist Wisdom: The Diamond Sutra and the Heart Sutra* by Edward Conze, p. 69.)

Katagiri Roshi comments on that verse extensively in [“*Diamond Sutra*, Talk 45: Final Lecture” (July 23, 1980)](https://katagiritranscripts.net/1980-07-23-Diamond-Sutra-Final-Lecture)

```{=typst}
#pagebreak()
```

# Chapter 29: Do Not Doubt the True Dragon

## Paragraph 14 Part 1

> 冀其參學高流、久習摸象。勿怪眞龍。  

> Please, honored followers of Zen, long accustomed to groping for the elephant, do not doubt the true dragon. [SZ] 

> Please, honored followers of Zen. Long accustomed to groping for the ele-
phant, do not be suspicious of the true dragon. [EB]

## Commentary

Katagiri Roshi mentions the story of the blind men touching the elephant, connecting it to a discussion of *saṃjñā* or “perception”:

> For instance, if you understand Zen, or Christianity, whatever. You have [an] experience of Christianity or Zen you understand. That is recognition. And then you put the mark on Christianity. That is *your* individual understanding. And then this individual understanding is really [to] *re-cognize*. You really re-cognize what kind of wood you need. Finally you say, “That is Christianity.” So you really attach to individual understanding. That is the function of perception. 
> 
> That is just like the blind men touching the elephant. There is an interesting story in the Buddhist scriptures: the king brings an elephant, and asks the blind men what it is. One blind man touches the ears of the elephant, and he says, “The elephant is just like a big fan.” Another is touching a leg, and says, “Oh, the elephant is just like a pillar!” *[He chuckles.]* Well, that is really the function of perception. 
>
> – From [“Karma: Taking Care of Karma,” July 4, 1980, at 45:24](https://katagiritranscripts.net/1980-07-04-Karma-Taking-Care-of-Karma#4524).

“True dragon” refers to the story of Seiko (or Shoko, Chinese: Yeh Kung-tzu), who loved images of dragons. But when a real dragon decided to visit him, Seiko was alarmed, and either scared the dragon off or ran away, depending on who’s telling the story.

```{=typst}
#pagebreak()
```

# Chapter 30: The Treasure Store

## Paragraph 14 Part 2

> 精進直指端的之道、尊貴絶學無爲之人。合沓佛佛之菩提、嫡嗣祖祖之三昧。久爲恁麼、須是恁麼、寶藏自開、受用如意。    

> Devote your energies to the way of direct pointing at the real. Revere the one who has gone beyond learning and is free from effort. Accord with the enlightenment of all the buddhas; succeed to the samadhi of all the ancestors. Continue to live in such a way, and you will be such a person. The treasure store will open of itself, and you may enjoy it freely. [SZ] 

> Devote your energies to a way that directly indicates the absolute. Revere the [person] of complete attainment who is beyond all human agency. Gain accord with the enlightenment of the buddhas; succeed to the legitimate lineage of the patriarchs' samadhi. Constantly perform in such a manner and you are assured of being a person such as they. Your treasure-store will open of itself, and you will use it at will. [EB]

## Commentary

In Chinese, *wu wei* (無爲) is translated here as “free from effort” or “beyond all human agency” – is a philosophical term literally meaning “not-acting” or “not-doing” (souce: [Wikipedia: “Wu wei”](https://en.wikipedia.org/wiki/Wu_wei)). In Japanese the term is *mui*; it translates the Sanskrit term *asamskrita*, and is also translated as “unconditioned,” and has the same meaning as “unconstructed.” (*Moon in a Dewdrop*, glossary, p. 346.)


More from 1986-03-19-Principles-of-Practice-Talk-1:

> So, “*sanzen gakudō* is the great matter of one’s whole life” [is my translation]. 
> 
> The “great” [is] *maha* in Sanskrit. *Maha* doesn’t mean something limited by human consciousness or human ideas. *Great* means *boundless*, or *immense*. 
> 
> And also we say “one’s *whole* life.” This *one’s whole life* is not *your* life in this world, but countless lives in an immensely long span of time, life after life. *The whole life* in this case [is] life after life. 
> 
> Because, what do you have to learn if you want to live in your spiritual life? You have to learn or study something more than your consciousness can see or your consciousness cannot see – [something] beyond this. [...] That means you have to learn the whole world. In the whole world, there are countless, countless beings [that] exist. So, the whole span of your lifetime is not good enough to learn all sentient beings in the whole world – because it’s very short! But we have to learn the *whole* world, *all* sentient beings. *How?* We have to spend this life and the other life and the other life... life after life. This is the meaning of the “one’s whole life” here. 
> 
> So, in this case, to learn the Buddha Way – to learn the Way – is not a small matter which [can] be learned at the university or in a workshop, et cetera. No; you cannot do it. The matter of learning the Way or studying the Way by surrendering yourself to the total tranquility is not a small matter – it’s really *boundless*, a *huge* matter, which you have to spend your life after life, you have to spend the immense long span of your time. 
> 
> This is the reason why Buddha is born in this world, the *Saddharma Pundarika Sutra* or *Lotus Sutra* says. Yes it is. [It is] why *you* were born; the same reason applies to the reason why you were born. Why were you born in this world? Because you are Buddha, we are Buddha. If so, the advent of your existence is due to seeing this great matter in your *whole* life. Life after life, we have to learn. 
> 
> This is the purpose of practice, the purpose of spiritual life. 
> 
> So what is the purpose of spiritual life? It is not the kind of individual experience [where] we usually believe that spiritual life is accompanied by mysterious or [miraculous] experiences. That is not the main purpose of spiritual life. You have to learn something *huge*. 
> 
> This is [the] purpose of spiritual life. That’s why in the *Prajñāpāramitā Sutra* we say we have to attain *anuttara-samyak-sambodhi*: the complete, perfect, supreme enlightenment. [This is] in the *Prajñāpāramitā* we chant every day. And then, you can attain *wisdom*, *prajñāpāramitā*. 
> 
> So in order to attain *anuttara-samyak-sambodhi*, perfect supreme enlightenment, that means you have to learn something more than you think or you cannot think. This is something very profound. 
> 
> Even though you don’t understand this, we are struggling [toward] attaining this. That’s why we practice. That’s why we live in this world. 




Katagiri Roshi says that the Way is a way to live. So the Way is not uppercase ‘W’, but lowercase ‘w’ as well:

> I mention constantly, if you really practice spiritual life, you cannot carry the spiritual life in terms of your understanding. If you want to practice spiritual life for the long run, you should live in vow. Vow means you should live your life in peace, in harmony, with deep, profound aspiration. Living in peace and harmony with all sentient beings.
> 
> Living in vow is not the big things you can expect, big things you can do. You cannot do big things. You cannot expect big things from your life. What you can do is just a little bit – just little, tiny things. When you get up in the morning, get up in the morning. Within the activity of getting up in the morning, there is a hallway to go through a door [into] the peaceful world. That’s why we have to take best care of the activity of getting up in the morning, doing zazen, having breakfast. This is a tiny activity for us. Everyone does it in that way. It’s not unusual. It’s not outstanding human activity. It’s very usual. But these kind of small details in human life can be seen in your everyday life all the way, always. So, where is [there a] door going [to] the peaceful world? [The] door is your everyday life. 
>
> So [...] I constantly say, vow is to just form habits of doing small details in your everyday life. But a habit is constantly made with your desires, [and] a vow is a not a habit [made] with your desires. Living in vow is to do something, small things, carrying on forever, *without* any desires. 
> 
> That is a way to live. That’s why Dōgen Zenji says (in *Gakudō-yōjinshū*), “The Way is that the buddha-dharma must be practiced just for the buddha-dharma.” This is called the Way, or the Buddha Way. 
> 
> The Buddha Way or Way is our gold. Where we should build up [human life], what is the destination, what is the gold? This is a way. 
> 
> And also Dōgen Zenji saying that the Way is that buddha-dharma is practiced just for the buddha-dharma means when you do *gassho*, just do gassho, for the gassho. 
> 
> Where is the door to peace? Right under your feet. It’s not a big deal. It is a really small, tiny deal. And also we have to carry this tiny deal *forever* – and under all circumstances. Beyond the satisfaction of your desires, constantly you have to carry it. For what? For living in peace and harmony with all sentient beings. This is a vow. 
> 
> At that time, whatever happens, you never drift in the ocean of human life. You can sail across the ocean of human life. 
> 
> This is a point Dōgen Zenji mentions in the last sentence of the *Genjōkōan*. I will read it once again: 
>
>> The wind of Buddhism makes manifest the great earth’s goldenness, and makes ripen the sweet milk of the long rivers.
> 
> *The long rivers* is human life: the long journey of human life. 
> 
> But this long journey is really sweet milk. You don’t understand this, because you see your life covered with suffering, pain, et cetera. But Dōgen Zenji says, “Please accept or taste human life as sweet milk.” This is his very profound, deep aspiration for living in peace and harmony with all sentient beings.
> 
> So this last sentence is really [Dōgen’s vow], but not only Dōgen’s, this is buddhas’ and ancestors’ vow, to live.
> 
> And this is not a teaching limited by schools and sects and denominations, any kind of religion. This is universal. 






“If you follow this practice, your treasure chest will open of itself and you can use it at will” is discussed in Q&A in [“Bendōwa: Dōgen's Questions & Answers – Talk 4”](https://katagiritranscripts.net/1987-03-14-Bendowa-Talk-4) at [1:16:15](https://katagiritranscripts.net/1987-03-14-Bendowa-Talk-4#11615):

> ... Realization is unfolding naturally, if you practice like this, exactly. Can you believe it? *[He laughs.]* Well, believe it or not, if you *do* it. This is life. You have to do it. Otherwise you cannot facilitate the development of education, and personalities ... no way. Constantly you have to unfold your life. How can you unfold your life as a buddha? Not unfold “you” as covered with the egoistic sense, you know? That’s easy! *[He laughs.]* We always unfold ourselves covered with egoism... pretty easy. But not covered with egoism, [you have to unfold yourself as a buddha]. How do you do this? You cannot unfold yourself in the dualistic world. So very naturally, *one world*. It means, when you do gassho, then you can unfold your life as a buddha. What do you mean? Can you analyze? The moment when you analyze, “Yes I do, this is a buddha” – you know, immediately you analyze. But this action, activity, flow activity, so-called *gassho*, with wholeheartedness, with the true sincere heart, that is a buddha. Because you become peaceful. And also people are impressed very much. Even though [they] don’t have such a cultural background, people do [gassho]. 
>
> For instance, you know, Narasaki Roshi went back to Japan from here, and Minayishi-san told me [later in a] letter, [the stewardess] always expressed very humble, respectful attitude toward Narasaki Roshi – not toward Minayishi-san and Hokan-san, et cetera. *[Laughter.]* So he thought, “Why does she always take best care of Narasaki Roshi only, with respect and kindness?” And then he watched [Narasaki Roshi] very often, and he realized he always *gassho*ed very sincerely. Whenever the stewardess came and talked and gave us something, he always [said], “Thank you.” That’s it. Do you understand? 
> 
> So that is peace. That is to unfold yourself as a buddha. No partition between stewardess and Narasaki Roshi, or race, Americans and Narasaki Roshi. 
> 
> **Questioner:** Well, to me it seems like it would almost have to be a natural unfolding that was spontaneous, and not even a conscious thing, because as soon as I say “this is something I have to do,” then there’s me, the subject, and the object, and there’s immediately dualism, and you’ve immediately lost it. So as soon as I say, “I have to do it,” then you can’t do it. 
> 
> **Katagiri Roshi:** Yes, that’s why your cultural background which you have accumulated, and your education, really interrupts you, you know? *[He laughs.]* For instance, everyone is impressed by this sincere demonstration of human life like Narasaki Roshi. More or less everyone is impressed. But people don’t know how to react to this, because immediately they say, “Oh, I’m American; what do you mean [by] *gassho*?” – something like that. So immediately you [hesitate], stand off. That’s why education, customs, heredity, and your knowledge, really prevent you from unfolding yourself straightforwardly as a buddha. 
>
> So that’s why we need to practice again and again. That’s why buddhas and ancestors [say to] practice unceasingly. Anyway, we have to do it, without abating, practice. So even though cultural background immediately interrupts your straightforward practice, [still] we have to do it, again and again. That is to not abate our practice, constantly. 

```{=typst}
#pagebreak()
```
## Miscellaneous Pieces

Katagiri Roshi also discussed *shō* as “the activity of freedom” in [“*Gabyō*: Painting of a Rice Cake – Talk 1” at 43:27](https://katagiritranscripts.net/1986-12-01-Gabyo-Talk-1#4327), and in relation to the eight consciousnesses in [“*Genjōkōan*: Talk 2” at 1:08:08](https://katagiritranscripts.net/1987-06-06-Genjokoan-Talk-2#10808). These are worthwhile reading. There is also useful commentary on these lines in the book *Each Moment Is the Universe*, Chapter 6, “The Root of the Buddha Way.”



- and maybe all sentient beings


1986-03-08-Triple-Treasure-Lecture-1


From https://katagiritranscripts.net/1979-05-09-Diamond-Sutra-Introduction

So, who protects your life? Who makes it possible for your life to exist for twenty years? You? No. Something else.
That is really vastness.
This is called emptiness, philosophically speaking. And if you experience that emptiness, it is called buddha-nature. Or, plainly speaking, that is universal consciousness, or truth. Or sometimes, vastness.
And sometimes vastness is personalized, and it’s called Buddha – because we realize vastness of the universe [in] your life, where there is no distraction, no dichotomies, no discrimination. Completely peace; perfectly peace [and] harmony.





By “beyond conscious or unconscious worlds,” Katagiri Roshi basically means that it is true reality, beyond our mental conceptions about it, either conscious or unconscious. In the context of explaining Dōgen’s *Genjōkōan*, Katagiri Roshi said: 

> “The Buddha Way” (佛道) means *true reality*. Practically, or truly, you live there, which is a bigger scale of the world than you have thought. That is the Buddha Way. 
>
> – From [“A, B, and C Worlds” (June 27, 1987) at 14:50](https://katagiritranscripts.net/1987-06-27-A-B-and-C-Worlds#1450).




There is a sense of something that is always *going*, and our job, if there is one, is to be *on it*.


Basically, “the Buddha Way” and “the Way” appear to be the same. 




- move this elsewhere:

A random example would be his commentary on  [“*Blue Cliff Record* Case 50: Yun Men’s Every Atom Samadhi”](https://katagiritranscripts.net/1984-01-04-Blue-Cliff-Record-Case-50), which lines up very well with this discussion:

> > A monk asked Yun Men, “What is every atom samadhi?”  
> > Men said, “Food in the bowl, water in the bucket.”  
>
> *Samadhi* means total acceptance. *Total acceptance* means you and all sentient beings are exactly in mutual accord. Zazen and you are exactly in mutual accord. There is no space, no gap between [which] you can poke your head into. That is so-called *samadhi*: “one-pointedness” or “concentration,” we say. Concentration or one-pointedness.

...

> So every atom, the original nature of each being, exists – interconnected, interpenetrated – [with] all sentient beings, without having its own substantiality, [its own] fixed entity. 
>
> That is called the “every atom samadhi.” *Samadhi* is total acceptance of your presence, your whole world, simultaneously. That is called *samadhi*. 
> 
> When you accept zazen totally, without creating any gap, within this practice there is a rhythm of the whole universe. That’s why even though people live around you, and there is the sound of the car outside of the building, it doesn’t bother your zazen, your concentration. You exactly fit into zazen rhythm, and also the rhythm of the whole world. That is called *samadhi*. 
> 
> So that *samadhi* must be each existence, each being. Microphone, your gassho, your washing your face, and your zazen, your walking on the street, your studies. 

More on kannō-dōkō: from 1982-12-01-Blue-Cliff-Record-Case-36-Talk-1

When you learn something from the mountains’ life, at that time it’s really something wonderful. Something more than joy, but anyway, joy. Or in Zen, maybe that is called enlightenment; *satori*. 

*Satori* is not something complicated you have to learn. Satori is found in the very simple movement which is exactly fit into the rhythm of life. [You and the mountains] fit together; at that time there is full communication between you and the mountains. That is called *kannō-dōkō* in Japanese. 

*Kan* means *perception*, literally. Perception means not only [through] the six senses, not only through consciousness; perception means to receive the mountains with your whole body, which exists in the present and the past and the future. So if you perceive the mountains with your whole body, which has been handed down from generation to generation, from the past to the present to the future, at that time you have really great communication. That is *nō* of *kannō*. *Nō* means *respond*. So you have to respond, but respond to the mountains with your whole body. 

When your whole body responds to the mountains’ life, at that time it is called *inspiration*. [It is] something more than you think you want to know, but it is represented as lots of questions in your life, those inspirations. Many things in the world of inspiration are kind of questions, lots of questions you don’t know [the answer to]. Like, “What’s that?” All these questions come up. Those questions are not something you can resolve in the realm of intellect or with intellectual research, but only within movement, only within responding to the rhythm of life which mountains have. If you really respond to this, that response is not a kind of intellectual inspiration, it’s movement. So within the movement, there is full communication there. That is to climb the mountains. 

So when you are completely drawn in by the mountains and living with the mountains, your living is exactly identical with that of the mountains, and you have to die exactly with the mountains, be alive with the mountains. If you do this, very naturally within each movement, responding to the voiceless voice that the mountain has, there is wonderful inspiration, so-called *learning*, learning  the mountains. It is more than intellectual research. It is not a sort of “big” thing or [fourth] dimension, it’s really simple. Apparently it’s just like the same things: religiously speaking, Katagiri is Katagiri, mountains are mountains, nothing different. But within the materialistic aspect of Katagiri and mountains, there is an enormous function of communication between you and mountains. 
