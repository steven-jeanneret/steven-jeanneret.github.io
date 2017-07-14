---
layout: post
title:  "Modification du thème Sublime Text 3"
date:   2017-07-14 19:50:00 +0200
categories: "Sublime-Text-3"
---

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>author</key>
	<string>Ihor Oleksandrov</string>
	<key>colorSpaceName</key>
	<string>sRGB</string>
	<key>name</key>
	<string>Boxy Tomorrow</string>
	<key>semanticClass</key>
	<string>boxy.tomorrow.dark</string>
	<key>settings</key>
	<array>
		<dict>
			<key>settings</key>
			<dict>
				<key>activeGuide</key>
				<string>#ffffff55</string>
				<key>background</key>
				<string>#1d1f21</string>
				<key>caret</key>
				<string>#c5c8c6</string>
				<key>foreground</key>
				<string>#c5c8c6</string>
				<key>guide</key>
				<string>#ffffff25</string>
				<key>gutter</key>
				<string>#1d1f21</string>
				<key>invisibles</key>
				<string>#969896</string>
				<key>lineHighlight</key>
				<string>#ffffff10</string>
				<key>popupCss</key>
				<string>
					html {
					  background-color: #2a2b2d;
					  color: #c5c8c6;
					}

					a {
					  color: #81a2be;
					}

					.error,
					.deleted {
					  color: #cc6666;
					}

					.success,
					.inserted,
					.name {
					  color: #b5bd68;
					}

					.warning,
					.modified {
					  color: #f0c674;
					}

					.type {
					  color: #8abeb7;
					  font-style: italic;
					}

					.param {
					  color: #de935f;
					}

					.current {
					  text-decoration: underline;
					}
				</string>
				<key>selection</key>
				<string>#ffffff16</string>
				<key>selectionBorder</key>
				<string>#ffffff16</string>
				<key>stackGuide</key>
				<string>#ffffff40</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Comments</string>
			<key>scope</key>
			<string>comment, punctuation.definition.comment</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>italic</string>
				<key>foreground</key>
				<!-- Couleur des commentaires -->
				<string>#3D9C4E</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Variable</string>
			<key>scope</key>
			<string>variable, string constant.other.placeholder</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<!-- Couleur noms des variables -->
				<string>#3F435A</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Invalid</string>
			<key>scope</key>
			<string>invalid</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#cc6666</string>
				<key>foreground</key>
				<string>#ffffff</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Invalid</string>
			<key>scope</key>
			<string>invalid.deprecated</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#b294bb</string>
				<key>foreground</key>
				<string>#ffffff</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Keyword, Storage</string>
			<key>scope</key>
			<string>keyword, storage.type, storage.modifier</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<!-- Mots clés virtual return class -->
				<string>#5C5C5B</string>
				<key>fontStyle</key>
				<string>italic</string>
				
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Operator, Misc</string>
			<key>scope</key>
			<string>keyword.operator, constant.other.color, punctuation, meta.tag, punctuation.definition.tag, punctuation.separator.inheritance.php, punctuation.definition.tag.html, punctuation.definition.tag.begin.html, punctuation.definition.tag.end.html, punctuation.section.embedded, keyword.other.template, keyword.other.substitution</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<!-- Couleurs opérateurs -->
				<string>#A4A8A7</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Tag</string>
			<key>scope</key>
			<string>entity.name.tag, meta.tag.sgml, markup.deleted.git_gutter</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<!-- Balises? -->
				<string>#d75a64</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Function, Special Method, Block Level</string>
			<key>scope</key>
			<string>entity.name.function, variable.function, support.function, keyword.other.special-method, meta.block-level</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<!-- Noms des fonctions -->
				<string>#324ACD</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Other Variable, String Link</string>
			<key>scope</key>
			<string>support.other.variable, string.other.link</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#d75a64</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Number, Constant, Function Argument, Tag Attribute, Embedded</string>
			<key>scope</key>
			<string>constant.numeric</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<!-- Valeurs constantes -->
				<string>#52CBA2</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>String, Symbols, Inherited Class, Markup Heading</string>
			<key>scope</key>
			<string>string, constant.other.symbol, constant.other.key,  markup.heading, markup.inserted.git_gutter, meta.group.braces.curly constant.other.object.key.js string.unquoted.label.js</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>normal</string>
				<key>foreground</key>
				<!-- String -->
				<string>#2B5034</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Class, Support</string>
			<key>scope</key>
			<string>entity.name.class, entity.name.type.class, support.type, support.class, support.other.namespace.use.php, meta.use.php, support.other.namespace.php, markup.changed.git_gutter, entity.other.inherited-class</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<!-- Nom de classe -->
				<string>#0A9383</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Sub-methods</string>
			<key>scope</key>
			<string>entity.name.module.js, variable.import.parameter.js, variable.other.class.js</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Language methods</string>
			<key>scope</key>
			<string>variable.language</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>italic</string>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>entity.name.method.js</string>
			<key>scope</key>
			<string>entity.name.method.js</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#81a2be</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>meta.method.js</string>
			<key>scope</key>
			<string>meta.class-method.js entity.name.function.js, variable.function.constructor</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#81a2be</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Attributes</string>
			<key>scope</key>
			<string>entity.other.attribute-name</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b294bb</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Inserted</string>
			<key>scope</key>
			<string>markup.inserted</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Deleted</string>
			<key>scope</key>
			<string>markup.deleted</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Changed</string>
			<key>scope</key>
			<string>markup.changed</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b294bb</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Regular Expressions</string>
			<key>scope</key>
			<string>string.regexp</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#8abeb7</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Escape Characters</string>
			<key>scope</key>
			<string>constant.character.escape</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#8abeb7</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>URL</string>
			<key>scope</key>
			<string>*url*, *link*, *uri*</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>underline</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Search Results Nums</string>
			<key>scope</key>
			<string>constant.numeric.line-number.find-in-files - match</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#a3685a</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Search Results Lines</string>
			<key>scope</key>
			<string>entity.name.filename.find-in-files</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Decorators</string>
			<key>scope</key>
			<string>tag.decorator.js entity.name.tag.js, tag.decorator.js punctuation.definition.tag.js</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>italic</string>
				<key>foreground</key>
				<string>#81a2be</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>ES7 Bind Operator</string>
			<key>scope</key>
			<string>source.js constant.other.object.key.js string.unquoted.label.js</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>italic</string>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 8</string>
			<key>scope</key>
			<string>source.json meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json string.quoted.double.json - meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json punctuation.definition.string - meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666bf</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 7</string>
			<key>scope</key>
			<string>source.json meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json string.quoted.double.json - meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json punctuation.definition.string - meta meta meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#81a2bebf</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 6</string>
			<key>scope</key>
			<string>source.json meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json string.quoted.double.json - meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json punctuation.definition.string - meta meta meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#f0c674bf</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 5</string>
			<key>scope</key>
			<string>source.json meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json string.quoted.double.json - meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json punctuation.definition.string - meta meta meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b294bbbf</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 4</string>
			<key>scope</key>
			<string>source.json meta meta meta meta meta meta meta meta.structure.dictionary.json string.quoted.double.json - meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta meta meta meta meta meta meta.structure.dictionary.json punctuation.definition.string - meta meta meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#de935f</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 3</string>
			<key>scope</key>
			<string>source.json meta meta meta meta meta meta.structure.dictionary.json string.quoted.double.json - meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta meta meta meta meta.structure.dictionary.json punctuation.definition.string - meta meta meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 2</string>
			<key>scope</key>
			<string>source.json meta meta meta meta.structure.dictionary.json string.quoted.double.json - meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta meta meta.structure.dictionary.json punctuation.definition.string - meta meta meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#81a2be</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 1</string>
			<key>scope</key>
			<string>source.json meta meta.structure.dictionary.json string.quoted.double.json - meta meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta meta.structure.dictionary.json punctuation.definition.string - meta meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#f0c674</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>JSON Key - Level 0</string>
			<key>scope</key>
			<string>source.json meta.structure.dictionary.json string.quoted.double.json - meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json, source.json meta.structure.dictionary.json punctuation.definition.string - meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.definition.string</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b294bb</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Plain</string>
			<key>scope</key>
			<string>text.html.markdown, punctuation.definition.list_item.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#c5c8c6</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Markup Raw Inline</string>
			<key>scope</key>
			<string>text.html.markdown markup.raw.inline</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#ffffff08</string>
				<key>foreground</key>
				<string>#c5c8c6cc</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Line Break</string>
			<key>scope</key>
			<string>text.html.markdown meta.dummy.line-break</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#ffffff50</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Heading</string>
			<key>scope</key>
			<string>markdown.heading, markup.heading | markup.heading entity.name, markup.heading.markdown punctuation.definition.heading.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#d75a64</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Italic</string>
			<key>scope</key>
			<string>markup.italic, markup.italic string</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>italic</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Bold</string>
			<key>scope</key>
			<string>markup.bold, markup.bold string</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Bold &amp; Italic</string>
			<key>scope</key>
			<string>markup.bold markup.italic, markup.italic markup.bold, markup.quote markup.bold, markup.bold markup.italic string, markup.italic markup.bold string, markup.quote markup.bold string</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold italic</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Underline</string>
			<key>scope</key>
			<string>markup.underline</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>underline</string>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Strike</string>
			<key>scope</key>
			<string>markup.strike</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>strike</string>
				<key>foreground</key>
				<string>#969896</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Blockquote</string>
			<key>scope</key>
			<string>markup.quote punctuation.definition.blockquote.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#ffffff16</string>
				<key>fontStyle</key>
				<string></string>
				<key>foreground</key>
				<string>#ffffff16</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Quote</string>
			<key>scope</key>
			<string>markup.quote</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>italic</string>
				<key>foreground</key>
				<string>#969896</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Link</string>
			<key>scope</key>
			<string>string.other.link.title.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#81a2be</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Link Description</string>
			<key>scope</key>
			<string>string.other.link.description.title.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b294bb</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Link Anchor</string>
			<key>scope</key>
			<string>constant.other.reference.link.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#f0c674</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Raw Block</string>
			<key>scope</key>
			<string>markup.raw.block</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#1D1F21</string>
				<key>foreground</key>
				<string>#c5c8c6cc</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Raw Block Fenced</string>
			<key>scope</key>
			<string>markup.raw.block.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#ffffff08</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Fenced Bode Block</string>
			<key>scope</key>
			<string>punctuation.definition.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#ffffff08</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Fenced Bode Block Variable</string>
			<key>scope</key>
			<string>markup.raw.block.fenced.markdown, variable.language.fenced.markdown, punctuation.section.class.end</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#c5c8c6</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Fenced Bode Block Punctuation</string>
			<key>scope</key>
			<string>punctuation.definition.fenced.markdown, meta.definition.language.raw.block.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string></string>
				<key>foreground</key>
				<string>#ffffff50</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Fenced Language</string>
			<key>scope</key>
			<string>variable.language.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string></string>
				<key>foreground</key>
				<string>#969896</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Separator</string>
			<key>scope</key>
			<string>meta.separator</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#ffffff08</string>
				<key>fontStyle</key>
				<string>bold</string>
				<key>foreground</key>
				<string>#969896</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markup - Table</string>
			<key>scope</key>
			<string>markup.table</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#ffffff08</string>
				<key>foreground</key>
				<string>#c5c8c6cc</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Punctuation Definition</string>
			<key>scope</key>
			<string>text.html.markdown punctuation.definition, text.html.markdown.note punctuation.definition.list_item.markdown, markup.table.markdown punctuation.definition.table.vertical-line.markdown, text.html.markdown markup.checkbox.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string></string>
				<key>foreground</key>
				<string>#ffffff50</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - HTML Punctuation Definition</string>
			<key>scope</key>
			<string>text.html.markdown meta.disable-markdown punctuation.definition</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#8abeb7</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - TODO Done</string>
			<key>scope</key>
			<string>punctuation.definition.list_item.todo.done</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - TODO Cancelled</string>
			<key>scope</key>
			<string>punctuation.definition.list_item.todo.cancelled</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - TODO GitHub Checkbox</string>
			<key>scope</key>
			<string>markup.checkbox.markdown markup.checkbox.checked_symbol.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Section Title</string>
			<key>scope</key>
			<string>markup.admonition.markdown string.other.admonition.title.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold</string>
				<key>foreground</key>
				<string>#c5c8c6</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Header</string>
			<key>scope</key>
			<string>markup.admonition.markdown markup.admonition.header.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#9f74ab50</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Body</string>
			<key>scope</key>
			<string>markup.admonition.markdown markup.admonition.body.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#9f74ab15</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Punctuation</string>
			<key>scope</key>
			<string>markup.admonition.markdown punctuation.definition.admonition.markdown, markup.admonition.markdown punctuation.definition.heading,markup.admonition.markdown punctuation.definition.table.vertical-line, markup.admonition.markdown punctuation.definition.table.horizontal-line, markup.admonition.markdown punctuation.definition.table.alignments, markup.admonition.markdown punctuation.definition.heading, markup.admonition.markdown punctuation.definition.bold, markup.admonition.markdown punctuation.definition.italic, markup.admonition.markdown punctuation.definition.list_item, markup.admonition.markdown punctuation.definition.raw, markup.admonition.markdown markup.checkbox.markdown, markup.admonition.markdown punctuation.definition.list_item.todo.pending, markup.admonition.markdown meta.link punctuation.definition, markup.admonition.markdown meta.link.inline markup.underline.link, markup.admonition.markdown meta.link.reference.markdown constant.other.reference.link.markdown, markup.admonition.markdown punctuation.definition.entity.html, markup.admonition.markdown meta.separator.markdown, markup.admonition.markdown markup.table.markdown punctuation.definition.table.vertical-line.markdown, markup.admonition.markdown meta.definition.language.raw.block.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#9f74ab75</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Section Type</string>
			<key>scope</key>
			<string>markup.admonition.markdown entity.name.admonition.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold</string>
				<key>foreground</key>
				<string>#9f74ab</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Element Background</string>
			<key>scope</key>
			<string>markup.admonition.markdown markup.table, markup.admonition.markdown markup.raw, markup.admonition.markdown markup.raw.block.fenced meta.language, markup.admonition.markdown punctuation.definition.blockquote.markdown, markup.admonition.markdown meta.separator, markup.admonition.markdown markup.raw.inline, markup.admonition.markdown markup.raw.block</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#9f74ab25</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Quote</string>
			<key>scope</key>
			<string>markup.admonition.markdown markup.quote punctuation.definition.blockquote.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#9f74ab35</string>
				<key>foreground</key>
				<string>#9f74ab35</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Header (Hint)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.hint markup.admonition.header.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#81a2be50</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Body (Hint)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.hint markup.admonition.body.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#81a2be15</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Punctuation (Hint)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.hint punctuation.definition.admonition.markdown, markup.admonition.markdown.hint punctuation.definition.heading,markup.admonition.markdown.hint punctuation.definition.table.vertical-line, markup.admonition.markdown.hint punctuation.definition.table.horizontal-line, markup.admonition.markdown.hint punctuation.definition.table.alignments, markup.admonition.markdown.hint punctuation.definition.heading, markup.admonition.markdown.hint punctuation.definition.bold, markup.admonition.markdown.hint punctuation.definition.italic, markup.admonition.markdown.hint punctuation.definition.list_item, markup.admonition.markdown.hint punctuation.definition.raw, markup.admonition.markdown.hint markup.checkbox.markdown, markup.admonition.markdown.hint punctuation.definition.list_item.todo.pending, markup.admonition.markdown.hint meta.link punctuation.definition, markup.admonition.markdown.hint meta.link.inline markup.underline.link, markup.admonition.markdown.hint meta.link.reference.markdown constant.other.reference.link.markdown, markup.admonition.markdown.hint punctuation.definition.entity.html, markup.admonition.markdown.hint meta.separator.markdown, markup.admonition.markdown.hint markup.table.markdown punctuation.definition.table.vertical-line.markdown, markup.admonition.markdown.hint meta.definition.language.raw.block.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#81a2be75</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Section Type (Hint)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.hint entity.name.admonition.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold</string>
				<key>foreground</key>
				<string>#81a2be</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Element Background (Hint)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.hint markup.table, markup.admonition.markdown.hint markup.raw, markup.admonition.markdown.hint markup.raw.block.fenced meta.language, markup.admonition.markdown.hint punctuation.definition.blockquote.markdown, markup.admonition.markdown.hint meta.separator, markup.admonition.markdown.hint markup.raw.inline, markup.admonition.markdown.hint markup.raw.block</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#81a2be25</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Quote (Hint)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.hint markup.quote punctuation.definition.blockquote.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#81a2be35</string>
				<key>foreground</key>
				<string>#81a2be35</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Header (Warning)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.warning markup.admonition.header.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#f0c67450</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Body (Warning)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.warning markup.admonition.body.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#f0c67415</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Punctuation (Warning)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.warning punctuation.definition.admonition.markdown, markup.admonition.markdown.warning punctuation.definition.heading,markup.admonition.markdown.warning punctuation.definition.table.vertical-line, markup.admonition.markdown.warning punctuation.definition.table.horizontal-line, markup.admonition.markdown.warning punctuation.definition.table.alignments, markup.admonition.markdown.warning punctuation.definition.heading, markup.admonition.markdown.warning punctuation.definition.bold, markup.admonition.markdown.warning punctuation.definition.italic, markup.admonition.markdown.warning punctuation.definition.list_item, markup.admonition.markdown.warning punctuation.definition.raw, markup.admonition.markdown.warning markup.checkbox.markdown, markup.admonition.markdown.warning punctuation.definition.list_item.todo.pending, markup.admonition.markdown.warning meta.link punctuation.definition, markup.admonition.markdown.warning meta.link.inline markup.underline.link, markup.admonition.markdown.warning meta.link.reference.markdown constant.other.reference.link.markdown, markup.admonition.markdown.warning punctuation.definition.entity.html, markup.admonition.markdown.warning meta.separator.markdown, markup.admonition.markdown.warning markup.table.markdown punctuation.definition.table.vertical-line.markdown, markup.admonition.markdown.warning meta.definition.language.raw.block.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#f0c67475</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Section Type (Warning)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.warning entity.name.admonition.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold</string>
				<key>foreground</key>
				<string>#f0c674</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Element Background (Warning)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.warning markup.table, markup.admonition.markdown.warning markup.raw, markup.admonition.markdown.warning markup.raw.block.fenced meta.language, markup.admonition.markdown.warning punctuation.definition.blockquote.markdown, markup.admonition.markdown.warning meta.separator, markup.admonition.markdown.warning markup.raw.inline, markup.admonition.markdown.warning markup.raw.block</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#f0c67425</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Quote (Warning)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.warning markup.quote punctuation.definition.blockquote.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#f0c67435</string>
				<key>foreground</key>
				<string>#f0c67435</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Header (Danger)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.danger markup.admonition.header.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#cc666650</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Body (Danger)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.danger markup.admonition.body.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#cc666615</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Punctuation (Danger)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.danger punctuation.definition.admonition.markdown, markup.admonition.markdown.danger punctuation.definition.heading,markup.admonition.markdown.danger punctuation.definition.table.vertical-line, markup.admonition.markdown.danger punctuation.definition.table.horizontal-line, markup.admonition.markdown.danger punctuation.definition.table.alignments, markup.admonition.markdown.danger punctuation.definition.heading, markup.admonition.markdown.danger punctuation.definition.bold, markup.admonition.markdown.danger punctuation.definition.italic, markup.admonition.markdown.danger punctuation.definition.list_item, markup.admonition.markdown.danger punctuation.definition.raw, markup.admonition.markdown.danger markup.checkbox.markdown, markup.admonition.markdown.danger punctuation.definition.list_item.todo.pending, markup.admonition.markdown.danger meta.link punctuation.definition, markup.admonition.markdown.danger meta.link.inline markup.underline.link, markup.admonition.markdown.danger meta.link.reference.markdown constant.other.reference.link.markdown, markup.admonition.markdown.danger punctuation.definition.entity.html, markup.admonition.markdown.danger meta.separator.markdown, markup.admonition.markdown.danger markup.table.markdown punctuation.definition.table.vertical-line.markdown, markup.admonition.markdown.danger meta.definition.language.raw.block.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc666675</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Section Type (Danger)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.danger entity.name.admonition.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold</string>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Element Background (Danger)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.danger markup.table, markup.admonition.markdown.danger markup.raw, markup.admonition.markdown.danger markup.raw.block.fenced meta.language, markup.admonition.markdown.danger punctuation.definition.blockquote.markdown, markup.admonition.markdown.danger meta.separator, markup.admonition.markdown.danger markup.raw.inline, markup.admonition.markdown.danger markup.raw.block</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#cc666625</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Quote (Danger)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.danger markup.quote punctuation.definition.blockquote.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#cc666635</string>
				<key>foreground</key>
				<string>#cc666635</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Header (Attention)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.attention markup.admonition.header.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#b5bd6850</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Body (Attention)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.attention markup.admonition.body.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#b5bd6815</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Punctuation (Attention)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.attention punctuation.definition.admonition.markdown, markup.admonition.markdown.attention punctuation.definition.heading,markup.admonition.markdown.attention punctuation.definition.table.vertical-line, markup.admonition.markdown.attention punctuation.definition.table.horizontal-line, markup.admonition.markdown.attention punctuation.definition.table.alignments, markup.admonition.markdown.attention punctuation.definition.heading, markup.admonition.markdown.attention punctuation.definition.bold, markup.admonition.markdown.attention punctuation.definition.italic, markup.admonition.markdown.attention punctuation.definition.list_item, markup.admonition.markdown.attention punctuation.definition.raw, markup.admonition.markdown.attention markup.checkbox.markdown, markup.admonition.markdown.attention punctuation.definition.list_item.todo.pending, markup.admonition.markdown.attention meta.link punctuation.definition, markup.admonition.markdown.attention meta.link.inline markup.underline.link, markup.admonition.markdown.attention meta.link.reference.markdown constant.other.reference.link.markdown, markup.admonition.markdown.attention punctuation.definition.entity.html, markup.admonition.markdown.attention meta.separator.markdown, markup.admonition.markdown.attention markup.table.markdown punctuation.definition.table.vertical-line.markdown, markup.admonition.markdown.attention meta.definition.language.raw.block.fenced.markdown</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b5bd6875</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Section Type (Attention)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.attention entity.name.admonition.markdown</string>
			<key>settings</key>
			<dict>
				<key>fontStyle</key>
				<string>bold</string>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Element Background (Attention)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.attention markup.table, markup.admonition.markdown.attention markup.raw, markup.admonition.markdown.attention markup.raw.block.fenced meta.language, markup.admonition.markdown.attention punctuation.definition.blockquote.markdown, markup.admonition.markdown.attention meta.separator, markup.admonition.markdown.attention markup.raw.inline, markup.admonition.markdown.attention markup.raw.block</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#b5bd6825</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Markdown - Admonition Quote (Attention)</string>
			<key>scope</key>
			<string>markup.admonition.markdown.attention markup.quote punctuation.definition.blockquote.markdown</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#b5bd6835</string>
				<key>foreground</key>
				<string>#b5bd6835</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>AceJump Label</string>
			<key>scope</key>
			<string>acejump.label</string>
			<key>settings</key>
			<dict>
				<key>background</key>
				<string>#528bff</string>
				<key>foreground</key>
				<string>#ffffff</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>SublimeLinter Warning</string>
			<key>scope</key>
			<string>sublimelinter.mark.warning</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#f0c674</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>SublimeLinter Gutter Mark</string>
			<key>scope</key>
			<string>sublimelinter.gutter-mark</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#ffffff</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>SublimeLinter Error</string>
			<key>scope</key>
			<string>sublimelinter.mark.error</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>GitGutter Ignored</string>
			<key>scope</key>
			<string>markup.ignored.git_gutter</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#969896</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>GitGutter Untracked</string>
			<key>scope</key>
			<string>markup.untracked.git_gutter</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#969896</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>GitGutter Inserted</string>
			<key>scope</key>
			<string>markup.inserted.git_gutter</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>GitGutter Changed</string>
			<key>scope</key>
			<string>markup.changed.git_gutter</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#f0c674</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>GitGutter Deleted</string>
			<key>scope</key>
			<string>markup.deleted.git_gutter</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Default</string>
			<key>scope</key>
			<string>brackethighlighter.default</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b294bb</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Unmatched</string>
			<key>scope</key>
			<string>brackethighlighter.unmatched</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#cc6666</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Curly</string>
			<key>scope</key>
			<string>brackethighlighter.curly</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#9f74ab</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Round</string>
			<key>scope</key>
			<string>brackethighlighter.round</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#f0c674</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Square</string>
			<key>scope</key>
			<string>brackethighlighter.square</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#81a2be</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Angle</string>
			<key>scope</key>
			<string>brackethighlighter.angle</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#de935f</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Tag</string>
			<key>scope</key>
			<string>brackethighlighter.tag</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#8abeb7</string>
			</dict>
		</dict>
		<dict>
			<key>name</key>
			<string>Bracket Highlighter Quote</string>
			<key>scope</key>
			<string>brackethighlighter.quote</string>
			<key>settings</key>
			<dict>
				<key>foreground</key>
				<string>#b5bd68</string>
			</dict>
		</dict>
	</array>
	<key>uuid</key>
	<string>21bb5fd7-098f-4cdd-86d7-f0b1a4a508ff</string>
</dict>
</plist>
```