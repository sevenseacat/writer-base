require 'asciidoctor'

guard 'shell' do
  watch(/^source\/(.+)\.adoc$/) do |m|
    Asciidoctor.render_file('source/base.adoc',
      to_file: "generated/base.html",
      safe: :unsafe,
    )

    `asciidoctor-pdf source/base.adoc -o generated/base.pdf`
  end
end
