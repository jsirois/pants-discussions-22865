python_requirements(name="reqs")

pex_binary(
    name="fortune",
    script="fortune",
    dependencies=[
        "configuration/riddles.dat",
        ":reqs#fortune",
    ],
    include_tools=True,
    args=["{pex.env.FORTUNE_FILE}"],
    extra_build_args=[
        "--bind-resource-path",
        "FORTUNE_FILE=configuration/riddles.dat",
    ]
)
